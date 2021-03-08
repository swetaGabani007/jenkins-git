String DEPLOYMENT_ENV_FAST = "FAST"
String DEPLOYMENT_ENV_FULL = "FULL"
properties (
        [
                [
                        $class: 'ParametersDefinitionProperty', parameterDefinitions:
                        [
                                [
                                        $class: 'ChoiceParameterDefinition',
                                        choices: DEPLOYMENT_ENV_FAST + '\n' + DEPLOYMENT_ENV_FULL,
                                        description: 'Select the kind of deployment you want',
                                        name: 'PDS_DEPLOYMENT_KIND_ENV'
                                ]
                        ]
                ],
                [
                        $class  : 'jenkins.model.BuildDiscarderProperty', strategy:
                        [
                                $class: 'LogRotator',
                                numToKeepStr: '10'
                        ]
                ]
        ]
)


pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
