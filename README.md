# Quality

graph LR
    A[Backlog] -->|Planning| B[Dev]
    B -->|Commit no Repo| C{CI Pipeline}
    C -->|Build| D[Tester]
    D -->|Testes Manuais<br>(Jira/Xray)| E[Report de Bugs]
    E --> B & F[QA]
    F -->|Automação Básica<br>(Selenium/Postman)| C
    F -->|Demanda Complexa| G[SDET]
    G -->|Framework Avançado<br>(Cypress+LoadRunner)| H[CD Pipeline]
    H -->|Deploy em Staging| D & I[Monitoramento]
    I -->|Logs + Grafana| J[Cliente]
