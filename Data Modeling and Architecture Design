# Week 1 – Data Modeling and Architecture Design

## Executive Overview

This week establishes the relational database foundation for a virtual retail environment. The objective is to translate retail business requirements into a logical, normalized and scalable SQL data model covering customers, products, suppliers, inventory, orders, order items and payments.

## Business Requirements

The database should support customer registration, product catalog management, supplier relationships, stock tracking, order processing, sales reporting and customer relationship management. The design must preserve data integrity and support operational queries efficiently.

## Core Entities

Customers: customer_id, name, email, phone, address, registration_date. Products: product_id, product_name, category_id, supplier_id, unit_price, reorder_level. Categories: category_id, category_name. Suppliers: supplier_id, supplier_name, contact details. Inventory: inventory_id, product_id, warehouse_id, quantity_on_hand, last_updated. Orders: order_id, customer_id, order_date, status, total_amount. Order_Items: order_item_id, order_id, product_id, quantity, unit_price. Payments: payment_id, order_id, payment_date, method, amount, status. Warehouses: warehouse_id, warehouse_name, location.

## Relationships and Keys

Each entity receives a primary key. Orders reference Customers; Order_Items references Orders and Products; Products reference Categories and Suppliers; Inventory references Products and Warehouses; Payments reference Orders. Foreign-key constraints prevent orphan records and maintain referential integrity.

## Normalization

The design targets Third Normal Form. Repeating groups are separated, category and supplier information are stored once, and order-level information is separated from order-item details. This reduces duplication and update anomalies.

## ERD and Architecture

Conceptual relationship: CUSTOMER → ORDER → ORDER_ITEM → PRODUCT → CATEGORY; PRODUCT → SUPPLIER; PRODUCT → INVENTORY → WAREHOUSE; ORDER → PAYMENT. Architecture can use an operational relational database with a reporting layer consuming controlled views or extracts.

## Indexing and Scalability

Primary keys are indexed automatically in most engines. Foreign-key columns such as customer_id, product_id and order_id should be indexed when justified. Composite indexes can support common date/status filters. Large transaction tables can later use date partitioning.

## Security and Workflow

Use role-based access, constraints, transactions, backups and controlled access to customer fields. A typical workflow is customer order → order header → order items → inventory update → payment status → reporting.

## Expected Outcome

The Week 1 milestone is a complete logical retail data model with documented entities, relationships, keys, normalization decisions, architecture considerations and an ERD-ready structure.

