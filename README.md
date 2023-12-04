# Simple FaaS (Function as a Service) using node with supabase
### Description
A simple implementation of FaaS (Function as a Service) using node with supabase. This project is based on the tutorial from [this page](https://dev.to/documatic/guide-to-implementing-function-as-a-service-a-deep-dive-into-serverless-computing-55gd)

### How to run
1. Clone this repository
2. Change the directory to the cloned repository
3. Run `npm install`
4. npx supabase link --project-ref your-project-ref
where your-project-ref is the project reference from your supabase project (Project Settings -> API -> Project URL (project-ref).supabase.co)
5. npx supabase functions deploy hello-world

### How to test
```bash
  curl --request POST 'https://<project_ref>.supabase.co/functions/v1/hello-world' \
      --header 'Authorization: Bearer ANON_KEY' \
      --header 'Content-Type: application/json' \
      --data '{ "name":"Functions" }'
```
where ANON_KEY is the anonymous key from your supabase project (Project Settings -> API -> Project API Keys)