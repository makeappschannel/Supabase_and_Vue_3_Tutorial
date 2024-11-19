# Supabase & Vue 3 Tutorial - Finished

This is the finished source code from the **Supabase & Vue 3 Tutorial** series on YouTube. Follow this guide to get the project running.

### Create Moneyballs Supabase Project

- Create a [Supabase](https://supabase.com) account
- From the Dashboard, click **New Project**
- On the **New Project** page:
  - Enter **Moneyballs** for the **Project name**
  - Generate a password (save it somewhere)
  - Choose a Region
  - Click **Create new project**:

![Supabase - Create new project](https://github.com/user-attachments/assets/a65a9736-e66b-4607-a596-bde8c6f06026)

### Create Entries Table

- Wait til your project is created
- On the side bar, click **Database**
- On the left, click **Tables**
- Click **New table**
- In Name, enter **entries**
- Disable **Enable Row Level Security (RLS)**
- Enable **Enable Realtime**
- Add the following columns (by clicking **Add column**):

| Name   | Type   | Default Value
| ------ | ------ | --- |
| name   | text   | (leave empty) |
| amount | float4 | 0 |
| paid   | bool   | false |
| order  | int8   | 1 |

![Supabase - Create Entries Table](https://github.com/user-attachments/assets/b0944bee-30a8-4f30-9774-023fdb834136)

- Click **Save**

### Add Supabase Config to Moneyballs

- On the left, click **Home**
- Scroll down to **Connecting to your new project**
- Copy the **Project URL** and the **API Key**:

![Supabase - Config](https://github.com/user-attachments/assets/a5ec2303-a7ca-4f68-8810-1f641d6a0b39)

- Open the file `/quasar.config.js`
- Find the `build > env` section
- Replace the **SUPABASE_URL** value with your **Project URL**
- Replace the **SUPABASE_ANON_KEY** value with your **API Key**:

```
build: {
  env: {
    SUPABASE_URL: 'https://ymharbyqitxhyxzuagys.supabase.co',
    SUPABASE_ANON_KEY: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InltaGFyYnlxaXR4aHl4enVhZ3lzIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MzIwMTg5MzQsImV4cCI6MjA0NzU5NDkzNH0.qqkzOtHSV_-zuGswNRaF1O4ibm-0tzxvd6yJMru2RG0'
  },
  ...
}
```

### Install the dependencies
```bash
yarn
# or
npm install
```

### Start the app in development mode
```bash
quasar dev
```
