# CLAUDE.md - business Repository

## Project Overview

The **business repository** stores **business and organization definitions** as MDX files with Zod schema validation via Velite, enabling bidirectional synchronization with the PostgreSQL database.

**Purpose**: Define and manage business entities as version-controlled MDX files that sync automatically to the database.

**Position**: 📝 **Content Layer** - Content source that syncs to db layer

## Schema

The Velite schema for business entities includes:

### Required Fields
- **title** (string): Business/organization name
- **description** (string): What the organization does

### Optional Fields
- **type** (string): Organization type (Corporation, LLC, Nonprofit, etc.)
- **industry** (string): Industry sector
- **founded** (string): Founding date
- **headquarters** (string): Location
- **employees** (number): Number of employees
- **revenue** (object): Revenue information
- **website** (URL): Company website
- **socialMedia** (array): Social media profiles
- **metadata**: Namespace and visibility
- **tags** (array): Categorization tags

## MDX File Example

```mdx
---
title: Acme Corporation
description: Provider of innovative software solutions
type: Corporation
industry: Software
founded: "2020"
headquarters: San Francisco, CA
employees: 50
website: https://acme.example.com
socialMedia:
  - twitter: acmecorp
  - linkedin: acme-corporation
metadata:
  ns: business
  visibility: public
tags:
  - software
  - saas
  - b2b
---

# Acme Corporation

Leading provider of enterprise software solutions for modern businesses.

## About

Founded in 2020, Acme Corporation helps businesses automate workflows and improve productivity.

## Products

- Workflow Automation
- Team Collaboration
- Analytics Platform
```

## Development Commands

```bash
# Install dependencies
pnpm install

# Build and validate all MDX files
pnpm build

# Watch mode for development
pnpm dev

# Type check
pnpm check-types
```

## Related Documentation

- **Parent**: [Root CLAUDE.md](../CLAUDE.md) - Multi-repo management
- **Database**: [db/CLAUDE.md](../db/CLAUDE.md) - Database schema and sync
- **API**: [api/CLAUDE.md](../api/CLAUDE.md) - Webhook handler
- **Brands**: [brands/CLAUDE.md](../brands/CLAUDE.md) - Related brand identities

---

**Last Updated**: 2025-10-03
**Maintained By**: Claude Code
**Repository**: https://github.com/dot-do/business
