# Sistema de Cardiologista ❤️

Aplicativo acadêmico em **Java** para registrar medições clínicas (pressão arterial, batimentos, etc.), com **importação/exportação em CSV** e interface simples (Swing). Projeto focado em prática de **POO** e manipulação de arquivos.

## 🎯 Objetivos
- Registrar medições clínicas por paciente
- Importar/exportar dados em **CSV**
- Facilitar visualização, busca e edição
- Exercitar POO, camadas e boas práticas

## 🧰 Stack
- Java 17+ (compatível com 11)
- Swing (GUI)
- Ant / Maven / Gradle (qualquer um — ver seção de build)
- Manipulação de arquivos CSV

## ✨ Funcionalidades
- CRUD de pacientes e medições
- Exportação/importação CSV
- Validações básicas
- Interface gráfica simples
- (Opcional) Acessibilidade: atalhos e foco

## 🗂️ Estrutura (sugerida após extrair o zip)
```
/src/...
/data/                 # dados CSV (git-ignored, use .example)
docs/                  # capturas de tela, diagramas
/dist/                 # artefatos de build (git-ignored)
```

## ▶️ Como executar

### Opção A) Via NetBeans
1. **Extraia** o conteúdo do `.zip` para a raiz do repositório (ou abra o projeto extraído).
2. Abra no NetBeans e execute o projeto.

### Opção B) Via linha de comando
- **Se houver `build.xml` (Ant):**
  ```bash
  ant clean dist
  ```
- **Se houver `pom.xml` (Maven):**
  ```bash
  mvn -B -DskipTests package
  ```
- **Se houver `build.gradle`:**
  ```bash
  ./gradlew build
  ```
- **Sem ferramenta de build (apenas fontes em `/src`):**
  ```bash
  find src -name "*.java" > sources.txt
  javac -d out @sources.txt
  java -cp out Main
  ```

> **CI**: O GitHub Actions detecta automaticamente Ant/Maven/Gradle. Se só houver `.java`, ele compila “na unha”. Se existir um `.zip` com o projeto, o CI **descompacta antes** de compilar.

## 📄 CSV (padrão sugerido)
- Arquivo: `data/medicoes.csv`
- Cabeçalho:
  ```
  paciente_id,nome,data,pressao_sistolica,pressao_diastolica,batimentos,observacao
  ```
- Codificação: UTF-8
- Separador: `,`
- Exemplos em `data/medicoes.csv.example`

## 🛣️ Roadmap
- [ ] Camada de serviço/repositório separada
- [ ] Testes unitários (JUnit)
- [ ] Exportar PDF/Excel
- [ ] Internacionalização (pt-BR/en)
- [ ] Persistência opcional com SQLite

## 🤝 Contribuição
Sinta-se à vontade para abrir issues e PRs! Padrões:
- Conventional Commits
- Branches: `feature/*`, `fix/*`
- PR com descrição clara e prints quando relevante

## 📜 Licença
Este projeto é licenciado sob **MIT**. Veja [LICENSE](LICENSE).
