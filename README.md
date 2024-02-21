# documentation

1 Transfert des databases de wordpress du cpanel vers un server
- Changer l'ancien nom du domain par le nouveau
- Importation de la base de donnée:
  docker exec -i container_name mysql -uuser -ppassword db_name < db.sql
- Changer le prefixe dans wp-config.php:
  $table_prefix = 'wp0t_';
- Importation du dossier wp-content

/* Add any custom values between this line and the "stop editing" line. */
define( 'FS_METHOD', 'direct' );
