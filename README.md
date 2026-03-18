# AWS PostgreSQL Integration & Troubleshooting Demo

Cloud Support Associate ready demo showing real-world RDS PostgreSQL setup, connectivity troubleshooting, performance tuning, and advanced features.

## Project Goal
Simulate customer-reported issues and demonstrate step-by-step diagnosis & resolution (exactly what the Cloud Support role does daily).

## Architecture
- EC2 (or local) → AWS RDS PostgreSQL
- VPC Security Groups + IAM database authentication
- Parameter groups for tuning

## Key Troubleshooting Scenarios Covered

1. **RDS Connection Timeout from Application**  
   - Diagnosed: Security Group rules, IAM auth vs password, endpoint resolution  
   - Fixed: Corrected inbound rules + switched to IAM auth

2. **Slow Queries**  
   - Used `EXPLAIN ANALYZE` to identify missing indexes  
   - Added B-tree + GIN indexes  
   - Tuned `work_mem`, `shared_buffers` via parameter group

3. **Connection Pooling & JSONB Handling**  
   - Implemented PgBouncer-style pooling demo  
   - Showed JSONB indexing for fast document queries

4. **Full-Text Search & Extensions**  
   - Enabled `pg_trgm` and `unaccent` extensions  
   - Built full-text search with `tsvector`

## Live Setup Steps (for recruiters)
1. Launch RDS PostgreSQL (free tier)  
2. Configure VPC Security Groups  
3. Enable IAM authentication  
4. Connect from Python/Flask or Node.js app  
5. Run `EXPLAIN ANALYZE` queries

## Screenshots
## Screenshots

### 1. RDS PostgreSQL Instance Details
![RDS Instance](screenshots/rds-instance.png)

### 2. EXPLAIN ANALYZE – Slow Query Diagnosis & Fix
![EXPLAIN ANALYZE Output](screenshots/explain-analyze.png)

### 3. VPC Security Group Rules (Port 5432 for RDS)
![Security Group Inbound Rules](screenshots/security-group.png)

*(Optional)*  
### 4. Graphical Query Plan View
![Graphical EXPLAIN](screenshots/explain-graphical.png)

## Technologies
AWS RDS PostgreSQL • VPC • IAM Database Auth • EXPLAIN/ANALYZE • JSONB • Full-text search • Parameter Groups

Repo created specifically for **Cloud Support Associate Internship – April 2026** application.
