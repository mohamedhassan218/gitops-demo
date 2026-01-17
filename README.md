# GitOps Demo

## About
This repository is a hands-on GitOps demo project built to practice and demonstrate the GitOps approach in a simple, practical way.

It is intentionally minimal and focuses on core GitOps concepts rather than production-level complexity.

This project is the practical companion to an article that explains GitOps concepts, motivations, and workflows: [click me]().


- Application code lives in `dev` and `prod`.
- Deployment state lives only in `gitops`.
- No application code is deployed directly, only GitOps changes are applied.
- The pipeline uses [skip ci] commits to avoid infinite loops.
- You can find built and pushed images here: [docker registry](https://hub.docker.com/repository/docker/mohassan218/gitops-demo/general)

## Repository Structure

```bash
.
├── dev/
│   ├── main.py
│   ├── test_main.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── prod/
│   ├── main.py
│   ├── test_main.py
│   ├── requirements.txt
│   └── Dockerfile
│
└── gitops/
    └── fastapi/
        ├── dev/
        │   └── values.yaml
        └── prod/
            └── values.yaml
```