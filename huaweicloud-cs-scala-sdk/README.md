# NAME

CloudStream Service API

实时流计算服（CloudStream Service，简称CS），是运行在华为云上的实时流式大数据分析服务，完全托管的方式让用户无需感知计算集群，只需聚焦于Stream SQL业务，即时执行作业，完全兼容Apache Flink API。

# VERSION

Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 
- Build date: 2018-01-30T14:26:04.654+08:00
- Build package: io.swagger.codegen.languages.AkkaScalaClientCodegen

# Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>com.huaweicloud.cs</groupId>
    <artifactId>huaweicloud-cs-scala.sdk</artifactId>
    <version>1.0-SNAPSHOT</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "com.huaweicloud.cs:huaweicloud-cs-scala.sdk:1.0-SNAPSHOT"
```

### SBT users

```scala
libraryDependencies += "com.huaweicloud.cs" % "huaweicloud-cs-scala.sdk" % "1.0-SNAPSHOT"
```

## Documentation for API Endpoints

All URIs are relative to *https://cs.cn-north-1.myhuaweicloud.com/v1.0*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthorizeApi* | [**authorizeBucket**](AuthorizeApi.md#authorizeBucket) | **POST** /{X-Project-Id}/obs_authorize | 用户主动授权起OBS桶的操作权限给CloudStream服务, 用于保存用户作业的checkpoint、作业的运行日志等
*ClusterApi* | [**createReservedCluster**](ClusterApi.md#createReservedCluster) | **POST** /{X-Project-Id}/reserved_cluster | 创建一个为具有cs_adm角色的CloudStream用户预留一个计算集群, 预留的集群会折算成SPU, 按需计费
*ClusterApi* | [**deleteReservedCluster**](ClusterApi.md#deleteReservedCluster) | **DELETE** /{X-Project-Id}/reserved_cluster/{cluster_id} | 删除预留的集群, 如果集群中有运行的作业会自动立即停止
*ClusterApi* | [**describeReservedCluster**](ClusterApi.md#describeReservedCluster) | **GET** /{X-Project-Id}/reserved_cluster/{cluster_id} | 查询用户创建的预留集群信息
*ClusterApi* | [**getClusterJobs**](ClusterApi.md#getClusterJobs) | **GET** /{X-Project-Id}/reserved_cluster/{cluster_id}/jobs | 查询预留集群下的作业列表
*ClusterApi* | [**getReservedClusters**](ClusterApi.md#getReservedClusters) | **GET** /{X-Project-Id}/reserved_clusters | 查询租户下的集群列表
*ClusterApi* | [**getUserQuota**](ClusterApi.md#getUserQuota) | **GET** /{X-Project-Id}/user_quota/{user_id} | 查询指定用户配额信息
*ClusterApi* | [**getUserQuotas**](ClusterApi.md#getUserQuotas) | **GET** /{X-Project-Id}/user_quotas | 获取租户下的用户配额信息
*ClusterApi* | [**updateReservedCluster**](ClusterApi.md#updateReservedCluster) | **PATCH** /{X-Project-Id}/reserved_cluster/{cluster_id} | 更新预留的集群
*ClusterApi* | [**updateUserQuota**](ClusterApi.md#updateUserQuota) | **PATCH** /{X-Project-Id}/user_quota/{user_id} | 更新指定用户配额信息
*JobApi* | [**deleteJob**](JobApi.md#deleteJob) | **DELETE** /{X-Project-Id}/job | 删除作业
*JobApi* | [**getJobDetail**](JobApi.md#getJobDetail) | **GET** /{X-Project-Id}/job/{job_id} | get job detail
*JobApi* | [**getJobExecuteGraph**](JobApi.md#getJobExecuteGraph) | **GET** /{X-Project-Id}/job/{job_id}/execute_graph | get job execution graph
*JobApi* | [**getJobs**](JobApi.md#getJobs) | **GET** /{X-Project-Id}/jobs | 查询作业列表
*JobApi* | [**runJob**](JobApi.md#runJob) | **POST** /{X-Project-Id}/job/run | 运行作业
*JobApi* | [**stopJob**](JobApi.md#stopJob) | **POST** /{X-Project-Id}/job/stop | Trigger to stop the running job
*JobApi* | [**submitJarJob**](JobApi.md#submitJarJob) | **POST** /{X-Project-Id}/jar_job | 创建一个用户自定义作业
*JobApi* | [**submitSqlJob**](JobApi.md#submitSqlJob) | **POST** /{X-Project-Id}/sql_job | 提交流式SQL作业到CloudStream服务
*JobApi* | [**updateJarJob**](JobApi.md#updateJarJob) | **PATCH** /{X-Project-Id}/jar_job | 更新用户自定义作业
*JobApi* | [**updateSqlJob**](JobApi.md#updateSqlJob) | **PATCH** /{X-Project-Id}/sql_job | 更新流式SQL作业
*LogApi* | [**getJobAuditLogs**](LogApi.md#getJobAuditLogs) | **GET** /{X-Project-Id}/audit_logs | query CloudStream Service job audit logs
*StatisticsApi* | [**overview**](StatisticsApi.md#overview) | **GET** /{X-Project-Id}/overview | 概要统计用户的作业和费用情况
*TemplateApi* | [**createJobTemplate**](TemplateApi.md#createJobTemplate) | **POST** /{X-Project-Id}/job_template | create the job template
*TemplateApi* | [**deleteJobTemplate**](TemplateApi.md#deleteJobTemplate) | **DELETE** /{X-Project-Id}/job_template/{template_id} | 删除作业模板
*TemplateApi* | [**getJobTemplates**](TemplateApi.md#getJobTemplates) | **GET** /{X-Project-Id}/job_templates | query CloudStream Service job templates


## Documentation for Models

 - [ClusterInfo](ClusterInfo.md)
 - [ClusterOverviewEntity](ClusterOverviewEntity.md)
 - [CreateClusterResponse](CreateClusterResponse.md)
 - [CreateClusterResponsePayload](CreateClusterResponsePayload.md)
 - [GetJobDetailResponse](GetJobDetailResponse.md)
 - [GlobalErrorResponse](GlobalErrorResponse.md)
 - [GlobalResponse](GlobalResponse.md)
 - [HeaderAuthorization](HeaderAuthorization.md)
 - [HeaderHost](HeaderHost.md)
 - [HeaderXAuthToken](HeaderXAuthToken.md)
 - [HeaderXProjectId](HeaderXProjectId.md)
 - [HeaderXSdkDate](HeaderXSdkDate.md)
 - [JobAuditLog](JobAuditLog.md)
 - [JobAuditLogResponse](JobAuditLogResponse.md)
 - [JobAuditLogResponsePayload](JobAuditLogResponsePayload.md)
 - [JobConfig](JobConfig.md)
 - [JobDetailEntity](JobDetailEntity.md)
 - [JobEntity](JobEntity.md)
 - [JobExecutePlan](JobExecutePlan.md)
 - [JobExecutePlanResponse](JobExecutePlanResponse.md)
 - [JobOverviewEntity](JobOverviewEntity.md)
 - [JobStatusInfo](JobStatusInfo.md)
 - [JobStatusResponse](JobStatusResponse.md)
 - [JobTemplate](JobTemplate.md)
 - [JobTemplateCreateResponse](JobTemplateCreateResponse.md)
 - [JobTemplateCreated](JobTemplateCreated.md)
 - [JobTemplateDeleteResponse](JobTemplateDeleteResponse.md)
 - [JobTemplateDeleted](JobTemplateDeleted.md)
 - [JobTemplateListResponse](JobTemplateListResponse.md)
 - [JobTemplateListResponsePayload](JobTemplateListResponsePayload.md)
 - [JobTemplateRequest](JobTemplateRequest.md)
 - [JobUpdateResponse](JobUpdateResponse.md)
 - [JobUpdateTime](JobUpdateTime.md)
 - [NewReservedClusterRequest](NewReservedClusterRequest.md)
 - [OverviewEntity](OverviewEntity.md)
 - [OverviewResponse](OverviewResponse.md)
 - [PathXProjectId](PathXProjectId.md)
 - [QueryClusterResponse](QueryClusterResponse.md)
 - [QueryClustersResponse](QueryClustersResponse.md)
 - [QueryClustersResponsePayload](QueryClustersResponsePayload.md)
 - [QueryJobListResponse](QueryJobListResponse.md)
 - [QueryJobListResponsePayload](QueryJobListResponsePayload.md)
 - [QueryUserQuotaResponse](QueryUserQuotaResponse.md)
 - [QueryUserQuotasResponse](QueryUserQuotasResponse.md)
 - [QueryUserQuotasResponsePayload](QueryUserQuotasResponsePayload.md)
 - [SubmitJarJobRequest](SubmitJarJobRequest.md)
 - [SubmitSqlJobRequest](SubmitSqlJobRequest.md)
 - [UpdateClusterRequest](UpdateClusterRequest.md)
 - [UpdateSqlJobRequest](UpdateSqlJobRequest.md)
 - [UpdateUserQuotaRequest](UpdateUserQuotaRequest.md)
 - [UserCluster](UserCluster.md)
 - [UserQuotaInfo](UserQuotaInfo.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:


# BUILDING YOUR LIBRARY

See the homepage `https://github.com/swagger-api/swagger-codegen` for full details.
But briefly, clone the git repository, build the codegen codebase, set up your build
config file, then run the API build script. You will need git, Java 7 or 8 and Apache
maven 3.0.3 or better already installed.

Your library files will be built under `WWW::MyProjectName`.

          $ git clone https://github.com/swagger-api/swagger-codegen.git
          $ cd swagger-codegen
          $ mvn package
          $ java -jar modules/swagger-codegen-cli/target/swagger-codegen-cli.jar generate \
    -i [URL or file path to JSON swagger API spec] \
    -l akka-scala \
    -c /path/to/config/file.json \
    -o /path/to/output/folder

Bang, all done. Run the `autodoc` script in the `bin` directory to see the API
you just built.

## Author

CloudStream@huawei.com
