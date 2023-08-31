# Sample inpuut

{
    "bucket_name":"awsace",
    "content_type":"text/plain",
	"object_name":"object100",
	"content":"This is my first object content"
}



---------------------------------------------------------------------
Stop Integration Node before executing mqsivault command
---------------------------------------------------------------------
mqsistop NODE1

---------------------------------------------------------------------
Execute mqsivault command
---------------------------------------------------------------------
mqsivault NODE1 --create --vault-key myvaultkey

---------------------------------------------------------------------
Start Integration Node after executing mqsivault command by providing vault-key
---------------------------------------------------------------------
mqsistart NODE1 --vault-key myvaultkey

---------------------------------------------------------------------
execute mqsicredentials command to store credentials in a vault
---------------------------------------------------------------------

amazons3: --secret-access-key <arg> --access-key-id <arg>


mqsicredentials NODE1 -e default --create --credential-name 'awss3_AmazonS31'  --credential-type 'amazons3'  --secret-access-key <arg> --access-key-id <arg>

---------------------------------------------------------------------
execute mqsicredentials command to report credentials in a vault
---------------------------------------------------------------------
mqsicredentials NODE1 -e default --report

---------------------------------------------------------------------
execute mqsivault command to decode credentials stored in a vault
---------------------------------------------------------------------
mqsivault NODE1 --decode credentials/odbc/DSN_NAME --vault-key myvaultkey

---------------------------------------------------------------------
execute mqsivault command to destroy credentials stored in a vault
---------------------------------------------------------------------
mqsivault NODE1 --destroy


#Below result from command

mqsicredentials --help
"
 The properties that are required for each credential vary depending on credential type. The list below shows the properties that are needed for each credential type:

amazoncloudwatch: --secret-access-key <arg> --access-key-id <arg>
amazonec2: --secret-access-key <arg> --access-key-id <arg>
amazonkinesis: --secret-access-key <arg> --access-key-id <arg>
amazonlambda: --secret-access-key <arg> --access-key-id <arg>
amazons3: --secret-access-key <arg> --access-key-id <arg>
amazonsqs: --secret-access-key <arg> --access-key-id <arg>
anaplan: --auth-type basic --username <arg> --password <arg>
anaplan: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
asana: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
azuread: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
azuread: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
azureblobstorage: --auth-type client --client-id <arg> --client-secret <arg>
azureblobstorage: --auth-type apiKey --api-key <arg>
box: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
calendly: --auth-type apiKey --api-key <arg>
calendly: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
cd: --username <arg> --password <arg>
cics: --auth-type basic --username <arg> --password <arg>
cics: --auth-type username --username <arg>
cloudantdb: --username <arg> --password <arg> --api-key <arg>
confluence: --username <arg> --api-key <arg>
coupa: --client-id <arg> --client-secret <arg>
dropbox: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
eis: --username <arg> --password <arg>
elk: --username <arg> --password <arg>
email: --username <arg> --password <arg>
eventbrite: --access-token <arg>
flexengage: --client-id <arg> --client-secret <arg>
ftp: --username <arg> --password <arg>
github: --auth-type privateKey --private-key <arg>
github: --auth-type accessKeyId --access-key-id <arg>
gmail: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
googlecalendar: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
googlecloudstorage: --secret-access-key <arg> --access-key-id <arg>
googledrive: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
googlepubsub: --private-key <arg> --client-email <arg>
http: --username <arg> --password <arg>
httpproxy: --username <arg> --password <arg>
ibmopenpages: --auth-type publicPrivateKeyPair --private-key <arg> --public-key <arg>
ibmopenpages: --auth-type basic --username <arg> --password <arg>
ims: --username <arg> --password <arg>
jdbc: --username <arg> --password <arg>
jenkins: --username <arg> --password <arg>
jira: --username <arg> --api-key <arg>
jms: --username <arg> --password <arg>
jndi: --username <arg> --password <arg>
kafka: --username <arg> --password <arg>
kerberos: --username <arg> --password <arg>
keystore: --password <arg>
keystorekey: --password <arg>
kronos: --username <arg> --password <arg> --api-key <arg> --client-id <arg> --client-secret <arg>
ldap: --username <arg> --password <arg>
local: --username <arg> --password <arg>
loopback: --auth-type basic --username <arg> --password <arg>
loopback: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
magento: --username <arg> --password <arg>
mailchimp: --access-token <arg>
marketo: --client-id <arg> --client-secret <arg>
maximo: --auth-type apiKeyWebsphere --api-key <arg> --websphere-username <arg> --websphere-password <arg>
maximo: --auth-type basicWebsphere --username <arg> --password <arg> --websphere-username <arg> --websphere-password <arg>
maximo: --auth-type basic --username <arg> --password <arg>
maximo: --auth-type apiKey --api-key <arg>
mondaydotcom: --api-key <arg>
mq: --username <arg> --password <arg>
mqtt: --username <arg> --password <arg>
msdynamicscrmrest: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
msdynamicscrmrest: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
msexcel: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
msexcel: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
msexchange: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
msonedrive: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
mssharepoint: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
mssharepoint: --auth-type basic --username <arg> --password <arg>
msteams: --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
odbc: --username <arg> --password <arg>
odm: --username <arg> --password <arg>
oracleebs: --username <arg> --password <arg>
oraclehcm: --username <arg> --password <arg>
rest: --auth-type basic --username <arg> --password <arg>
rest: --auth-type basicApiKey --username <arg> --password <arg> --api-key <arg>
rest: --auth-type apiKey --api-key <arg>
salesforce: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
salesforce: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
salesforcemc: --auth-type client --client-id <arg> --client-secret <arg>
salesforcemc: --auth-type oauth --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg>
sapariba: --username <arg> --password <arg>
sapodata: --username <arg> --password <arg>
servicenow: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
servicenow: --auth-type basic --username <arg> --password <arg>
sftp: --auth-type basic --username <arg> --password <arg>
sftp: --auth-type sshPublicKey --username <arg> --passphrase <arg> --ssh-identity-file <arg>
slack: --access-token <arg>
smtp: --username <arg> --password <arg>
snowflake: --username <arg> --password <arg>
soap: --username <arg> --password <arg>
trello: --client-id <arg> --access-token <arg>
truststore: --password <arg>
truststorekey: --password <arg>
userdefined: --username <arg> --password <arg> --api-key <arg> --passphrase <arg> --ssh-identity-file <arg> --client-id <arg> --client-secret <arg> --access-token <arg> --refresh-token <arg> --secret-access-key <arg> --access-key-id <arg> --websphere-username <arg> --websphere-password <arg> --private-key <arg> --public-key <arg> --public-key-id <arg> --client-email <arg>
wordpress: --access-token <arg>
wsrr: --username <arg> --password <arg>
wxs: --username <arg> --password <arg>
zendeskservice: --auth-type basicClientId --username <arg> --password <arg> --client-id <arg> --client-secret <arg>
zendeskservice: --auth-type basic --username <arg> --password <arg>
zendeskservice: --auth-type accessToken --access-token <arg>
zendeskservice: --auth-type usernameApiKey --username <arg> --api-key <arg>"
