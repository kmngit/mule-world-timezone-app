pipeline
{
	agent any
	stages
	{
		stage('Build:::World Timezone Application')
		{
			steps
			{
				bat 'mvn clean install'
			}
		}
		stage('Deploy:::World Timezone Application to CloudHub')
		{
			steps
			{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		stage('Regression Test:::World Timezone Application')
		{
			steps
			{
				bat 'C:\\Users\\Madhavan\\AppData\\Roaming\\npm\\newman run C:\\Users\\Madhavan\\Documents\\Postman\\Collections\\WorldTimeZone-Newman.postman_collection.json -r htmlextra --reporter-htmlextra-export C:\\Users\\Madhavan\\Documents\\Postman\\Collections --reporter-htmlextra-darkTheme'
			}
		}
	}
}