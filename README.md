## health_files

```sql
CREATE TABLE eh_healthfiles(
    health_file_id INT UNSIGNED NOT NULL AUTO_INCREMENT COMMENT 'Primary Key: Unique identifier for health file record',
    eh_health_file_id VARCHAR(20) DEFAULT NULL COMMENT '',
    eh_file_id VARCHAR(45) DEFAULT NULL COMMENT 'File ID for reference',
    eh_user_id VARCHAR(20) NOT NULL COMMENT 'External user ID for integration purposes',
    file_type VARCHAR(50) DEFAULT NULL COMMENT 'Type of file uploaded',
    category TEXT COMMENT '',
    sub_category VARCHAR(50) COMMENT '',
    file_lock bit(1) DEFAULT b'0' COMMENT '1 for active record and NULL for passive record',
    verify_status varchar(5) DEFAULT NULL COMMENT 'Verification status for file'
    error_code VARCHAR(5) DEFAULT NULL COMMIT 'Error Code'
    error_msg  TEXT COMMIT 'Error Message' 
    created_at DATETIME NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT 'Timestamp when the record was created',
    modified_on DATETIME DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP COMMENT 'Timestamp of the last update',
    deleted_at DATETIME DEFAULT NULL COMMENT 'Timestamp when the record was soft deleted',
    active_flag TINYINT(1) NOT NULL DEFAULT '1' COMMENT '1 for active record, 0 for inactive record',
);
```

