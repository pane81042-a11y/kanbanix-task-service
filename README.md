# Kanbanix Task Service

## Overview

The Kanbanix Task Service is a serverless backend microservice responsible for managing tasks within boards in the Kanbanix platform.

It supports task creation, updates, deletion, and status transitions while enforcing secure access using Amazon Cognito JWT authorization.

This service is designed to operate fully within the AWS Always Free Tier.

---

## Architecture

- AWS Lambda (Task business logic)
- Amazon API Gateway (REST API endpoints)
- Amazon DynamoDB (Task persistence)
- Amazon Cognito (Authentication and JWT validation)
- IAM roles with least privilege access

---

## Responsibilities

- Create tasks within boards
- Update task details and status
- Support drag-and-drop state transitions
- Retrieve board-specific tasks
- Delete tasks
- Enforce board ownership validation

---

## Security

- Cognito User Pool integration
- JWT-based authorization via API Gateway
- User identity extraction from token claims
- IAM-based least privilege permissions

---

## Deployment Model

Deployed independently as part of a distributed serverless microservices architecture.

All requests must include a valid Cognito access token in the Authorization header.

---

## Tech Stack

- Node.js
- AWS Lambda
- DynamoDB
- API Gateway
- Amazon Cognito

---

## Status

Initial service scaffolding and architecture configuration.
