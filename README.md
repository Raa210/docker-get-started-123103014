# docker-get-started-123103014

Tugas Docker Get Started memakai guide **Node.js** dari https://docs.docker.com/guides/nodejs/

## Isi

Aplikasi Express (TypeScript) dengan PostgreSQL di folder `nodejs-docker-example`.

## Yang dikerjakan

1. Containerize aplikasi Node.js (Dockerfile multi-stage, compose.yaml, .dockerignore)
2. Development dengan container: PostgreSQL, volume persisten, Compose Watch, debugging
3. Menjalankan test (Vitest) di dalam container

## Cara menjalankan

1. Install Docker Desktop dan login: `docker login dhi.io`
2. Buat file `nodejs-docker-example/db/password.txt` berisi `mysecretpassword`
   (file ini tidak ikut di-commit karena ada di .gitignore)
3. Jalankan:

   cd nodejs-docker-example
   docker compose up --build

4. Buka http://localhost:3000

## Menjalankan test

docker compose run --build --rm --no-deps server npm test
