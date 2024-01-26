# scripts

gcloud dataproc jobs submit pyspark --cluster=<CLUSTER_NAME> --region=<REGION> \
--archives '<gs://PATH/TO/dep_package.tar.gz>#deps' \
--properties=spark.submit.deployMode=cluster,spark.yarn.appMasterEnv.PYTHONPATH=deps,spark.executorEnv.PYTHONPATH=deps \
main.py
