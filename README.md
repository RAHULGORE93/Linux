

                              *************** Adding Retention to particuler folder by followig cron.d *****************

cd /etc/cron.d

[root@ANEEACOR01 cron.d]# more eea-adapters
 0 * * * * eea-besr find /data/cea_output/gpeh_input/               -type f -name "*.bin.gz" -mmin +480  -delete 2>/dev/null
 0 * * * * eea-besr find /data/cea_output/gpeh_staging/             -type f -name "*.bin.gz" -mmin +480  -delete 2>/dev/null
 0 * * * * eea-besr find /data/cea_output/gpeh_archive/             -type f -name "*.bin.gz" -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/epg_ebm_input/            -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/epg_ebm_staging/          -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/epg_ebm_archive/          -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/pgw_u_ebm_input/          -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/pgw_u_ebm_staging/        -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/pgw_u_ebm_archive/        -type f -name "*"        -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/sgsn_mme_ebm_input/       -type f -name "*_ebs.*"  -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/sgsn_mme_ebm_staging/     -type f -name "*_ebs.*"  -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/sgsn_mme_ebm_archive/     -type f -name "*_ebs.*"  -mmin +480  -delete 2>/dev/null
 5 * * * * eea-besr find /data/cea_output/sgsn_mme_ebm_direct_temp/ -type f                  -mmin +480  -delete 2>/dev/null
 7 * * * * eea-besr find /data/cea_output/ctr_input/                -type f -name "*"        -mmin +480  -delete 2>/dev/null
 7 * * * * eea-besr find /data/cea_output/ctr_staging/              -type f -name "*"        -mmin +480  -delete 2>/dev/null
 7 * * * * eea-besr find /data/cea_output/ctr_archive/              -type f -name "*"        -mmin +480  -delete 2>/dev/null
 9 * * * * eea-besr find /data/cea_output/ctum_input/               -type f -name "*"        -mmin +480  -delete 2>/dev/null
 9 * * * * eea-besr find /data/cea_output/ctum_staging/             -type f -name "*"        -mmin +480  -delete 2>/dev/null
 9 * * * * eea-besr find /data/cea_output/ctum_archive/             -type f -name "*"        -mmin +480  -delete 2>/dev/null
25 * * * * eea-besr find /data/cea_output/pag_tmp/                  -type f                  -mmin +480  -delete 2>/dev/null
42 * * * * eea-besr find /data/cea_output/archive/                  -type f                  -mmin +480  -delete 2>/dev/null
42 * * * * eea-besr find /data/cea_output/archive_gna/              -type f                  -mmin +480  -delete 2>/dev/null
42 * * * * eea-besr find /data/cea_output/input/                    -type f                  -mmin +480  -delete 2>/dev/null
42 * * * * eea-besr find /data/cea_output/output/                   -type f                  -mmin +480  -delete 2>/dev/null
42 * * * * eea-besr find /data/cea_output/pag/                      -type f                  -mmin +480  -delete 2>/dev/null
15 3 * * * eea-besr find /data/cea_output/                          -type d -empty           -mmin +2880 -delete 2>/dev/null
[root@ANEEACOR01 cron.d]#
[root@ANEEACOR01 cron.d]#
