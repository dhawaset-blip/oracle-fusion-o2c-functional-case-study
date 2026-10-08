# Order-to-Cash (O2C) Process Steps

## 1. Purpose

This document describes the end-to-end Order-to-Cash (O2C) process for NovaTech Electronics Pvt. Ltd.

The process follows the primary business scenario in which ABC Solutions Pvt. Ltd. places an order for electronic products with NovaTech.

The documented process covers:

Customer Order → Sales Order → Validation → Product Availability → Fulfillment → Shipment → Invoicing → Payment → Payment Application → Reconciliation

---

# 2. Primary Business Scenario

### Customer
ABC Solutions Pvt. Ltd.

### Supplier
NovaTech Electronics Pvt. Ltd.

### Order

| Product | Quantity | Unit Price | Line Value |
|---|---:|---:|---:|
| Business Laptop | 10 | ₹60,000 | ₹6,00,000 |
| 24-inch Monitor | 10 | ₹15,000 | ₹1,50,000 |
| Business Keyboard | 10 | ₹2,000 | ₹20,000 |
| Wireless Mouse | 10 | ₹1,500 | ₹15,000 |
| **Total** | **40 units** | | **₹7,85,000** |

---

# 3. End-to-End Process

## O2C-01 — Customer Places Order

### Description

ABC Solutions submits a request to purchase products from NovaTech.

### Responsible Function

Customer / Sales

### Input

- Customer information
- Product requirements
- Required quantities
- Delivery requirements

### Output

Customer order request

### Key Validation

The order request should contain sufficient information for order entry.

---

## O2C-02 — Create Sales Order

### Description

The Sales / Order Management team captures the customer's request as a sales order.

### Responsible Function

Sales / Order Management

### Input

- Customer details
- Product details
- Quantities
- Pricing information
- Delivery information

### Output

Sales order

### Key Validation

Required customer and order information must be available before the order progresses.

---

## O2C-03 — Validate Customer and Order

### Description

The order is reviewed to ensure that the customer and order information is valid.

### Responsible Function

Sales / Order Management

### Input

Sales order

### Validation Areas

- Customer validity
- Product validity
- Quantity
- Pricing
- Required order information
- Delivery information

### Decision

**Is the order valid?**

### If Yes

Proceed to product availability checking.

### If No

Correct the order information and perform validation again.

### Output

Validated sales order or identified exception

---

## O2C-04 — Check Product Availability

### Description

The requested products and quantities are checked to determine whether the order can be fulfilled.

### Responsible Function

Order Management / Warehouse

### Input

- Validated sales order
- Product
- Required quantity

### Decision

**Are the required products available?**

### If Yes

Proceed to fulfillment.

### If No

Route the order to the defined exception or backorder process.

### Output

Product availability status

---

## O2C-05 — Order Fulfillment

### Description

The fulfillment team prepares the confirmed products according to the sales order.

### Responsible Function

Warehouse / Fulfillment

### Input

- Validated sales order
- Available products
- Required quantities

### Output

Products prepared for shipment

### Key Validation

The products and quantities prepared for shipment should correspond to the confirmed order.

---

## O2C-06 — Shipment

### Description

The fulfilled products are prepared for delivery and shipped to the customer.

### Responsible Function

Shipping

### Input

- Fulfilled order
- Product and quantity information
- Customer delivery information

### Output

Shipment

### Key Validation

Shipment information should correspond to the fulfilled order and intended customer.

---

## O2C-07 — Generate Customer Invoice

### Description

An invoice is generated for the applicable customer transaction after the relevant fulfillment/invoicing conditions are satisfied.

### Responsible Function

Accounts Receivable

### Input

- Customer information
- Order information
- Fulfillment/shipment information
- Applicable pricing and charges

### Output

Customer invoice

### Key Validation

The invoice should accurately reflect the applicable transaction.

---

## O2C-08 — Customer Payment

### Description

ABC Solutions makes payment against the customer invoice.

### Responsible Function

Customer / Finance

### Input

- Customer invoice
- Payment information

### Output

Customer payment

---

## O2C-09 — Record / Apply Customer Payment

### Description

The received customer payment is recorded and applied to the appropriate customer receivable.

### Responsible Function

Accounts Receivable / Finance

### Input

- Customer payment
- Customer account
- Applicable invoice/receivable

### Output

Payment applied to customer receivable

### Key Validation

The payment should be associated with the correct customer and applicable receivable.

---

## O2C-10 — Payment Matching

### Description

The payment is checked against the relevant customer receivable.

### Responsible Function

Finance / Accounts Receivable

### Decision

**Does the payment match the receivable?**

### If Yes

Proceed to payment reconciliation.

### If No

Investigate the payment mismatch.

### Possible Mismatch Examples

- Incorrect payment amount
- Incorrect customer
- Incorrect invoice reference
- Partial payment
- Unidentified payment

---

## O2C-11 — Investigate Payment Mismatch

### Description

The Finance / Accounts Receivable team investigates discrepancies between the received payment and the expected receivable.

### Responsible Function

Finance / Accounts Receivable

### Possible Actions

- Review payment information
- Verify customer details
- Verify invoice reference
- Check outstanding balance
- Identify partial or excess payment
- Correct payment application where appropriate

### Output

Resolved or pending payment exception

---

## O2C-12 — Reconcile Payment

### Description

Once the payment is correctly matched and applied, the transaction is reconciled against the relevant customer receivable.

### Responsible Function

Finance / Accounts Receivable

### Input

- Applied customer payment
- Customer receivable
- Payment information

### Output

Reconciled payment

---

## O2C-13 — O2C Transaction Complete

### Description

The O2C transaction is considered complete when the order has progressed through fulfillment, shipment, invoicing and successful payment processing/reconciliation according to the defined business process.

### Final Business Outcome

- Customer order fulfilled
- Products shipped
- Invoice generated
- Payment received
- Payment correctly applied
- Receivable reconciled


# 4. O2C Process Summary

| Step ID | Process Activity | Responsible Function | Input | Output |
|---|---|---|---|---|
| O2C-01 | Customer Places Order | Customer / Sales | Product request | Order request |
| O2C-02 | Create Sales Order | Sales / Order Management | Customer + order details | Sales order |
| O2C-03 | Validate Customer and Order | Sales / Order Management | Sales order | Validated order / exception |
| O2C-04 | Check Product Availability | Order Management / Warehouse | Validated order | Availability status |
| O2C-05 | Order Fulfillment | Warehouse / Fulfillment | Validated order + products | Fulfilled order |
| O2C-06 | Shipment | Shipping | Fulfilled order | Shipment |
| O2C-07 | Generate Customer Invoice | Accounts Receivable | Order + fulfillment information | Customer invoice |
| O2C-08 | Customer Payment | Customer / Finance | Customer invoice | Payment |
| O2C-09 | Record / Apply Customer Payment | Finance / Accounts Receivable | Payment + receivable | Applied payment |
| O2C-10 | Payment Matching | Finance / Accounts Receivable | Payment + receivable | Match / mismatch |
| O2C-11 | Investigate Payment Mismatch | Finance / Accounts Receivable | Mismatch | Resolved/pending exception |
| O2C-12 | Reconcile Payment | Finance / Accounts Receivable | Applied payment | Reconciled payment |
| O2C-13 | O2C Transaction Complete | Finance / Business | Completed transaction | Closed transaction |