<p align="center">
  <img src="https://i.imgur.com/abc123.png" width="300" alt="Logo Panda IA Fitness">
  <h2 align="center">Panda IA Treinos Hipertrofia</h2>
</p>

[![Laravel](https://img.shields.io/badge/Laravel-12.49-brightgreen)](https://laravel.com)
[![PHP](https://img.shields.io/badge/PHP-8.2-blue)](https://php.net)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

App web que usa **IA GPT-4o-mini** para gerar treinos personalizados de **hipertrofia muscular** com análise **biomecânica detalhada**. TCC Educação Física 2º semestre + startup fitness.

![Screenshot](docs/sprint2-gpt.png)

## 🎯 Objetivo do TCC

Desenvolver e testar aplicativo de prescrição de treinos resistidos com IA, baseado em biomecânica e movimentos humanos, otimizando ganhos de hipertrofia em alunos de academia. [file:4]

## 🛠️ Stack Tecnológica

- **Backend**: Laravel 12.49 + PHP 8.2 (XAMPP)
- **Banco**: MySQL (`tcc_fitness`)
- **IA**: OpenAI GPT-4o-mini API (JSON exercícios + biomecânica)
- **Front**: Blade + Bootstrap 5 + Vite
- **Deploy**: Heroku/Vercel + Mercado Pago PRO

## 📁 Estrutura do Projeto

app/
├── Models/Treino.php # JSON: nome, séries, reps, biomecânica
├── Http/Controllers/TreinoController.php # GPT calls
resources/views/treinos/ # Form + Cards treinos
database/migrations/ # treinos + users

text

## 🚀 Como Rodar (Local)

1. Clone: `git clone https://github.com/SEU_USERNAME/tcc-ia-fitness.git`
2. `cd tcc-ia-fitness`
3. `composer install`
4. Copie `.env.example` → `.env` e configure:
DB_DATABASE=tcc_fitness
OPENAI_API_KEY=sk-proj-sua-chave

5. `php artisan key:generate`
6. `php artisan migrate`
7. `php artisan tinker` → Crie user:
```php
App\Models\User::create(['name'=>'Rodrigo','email'=>'coach@panda.com','password'=>bcrypt('123')]);
php artisan serve

http://localhost:8000/treinos → Gere treino IA!

📊 Sprints Concluídos
Sprint 1: MVP Base
Models/DB: users, treinos (JSON biomecânica)

Controller: Form gera/lista treinos

View: Bootstrap cards JSON [file:84]

Sprint 2: IA GPT Real
OpenAI GPT-4o-mini integrada

Prompt refinado: 4 exercícios ABC hipertrofia + torque/ângulos

Output: "Remada curvada – torque dorsal 90°" [file:89]

Próximos: MP R$29 PRO + testes 20 alunos (hipertrofia mensurada).

📈 Plano de Negócios
Plano	Preço	Features
Aluno Free	R$0	3 treinos/semana
Aluno PRO	R$29/mês	IA ilimitada + tracking
Coach PRO	R$99/mês	Dashboard alunos
📚 TCC Documentação
Pré-projeto: Objetivos/justificativa prontos.

Metodologia: Teste 8 semanas, n=20, medidas circunferência/força.

Prints: docs/screenshots/

🤝 Contribuições
Fork projeto

git checkout -b feature/nova-funcionalidade

Commit: git commit -m 'Adiciona X'

Push: git push origin feature/nova-funcionalidade

Abre Pull Request

📄 Licença
MIT – Veja LICENSE

🐼 Autor
Rodrigo Luiz da Silva Pinheiro
@panda.treinando.fofinho
TCC Ed. Física 2026 | Panda Suplementos
