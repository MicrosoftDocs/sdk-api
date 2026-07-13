---
UID: NS:devfiltertypes._DEVPROP_FILTER_EXPRESSION
tech.root: devinst
title: DEVPROP_FILTER_EXPRESSION
ms.date: 11/04/2024
targetos: Windows
description: Describes a filter expression used to query filter results.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: devfiltertypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DEVPROP_FILTER_EXPRESSION, *PDEVPROP_FILTER_EXPRESSION
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devfiltertypes.h
api_name:
 - _DEVPROP_FILTER_EXPRESSION
 - PDEVPROP_FILTER_EXPRESSION
 - DEVPROP_FILTER_EXPRESSION
f1_keywords:
 - _DEVPROP_FILTER_EXPRESSION
 - devfiltertypes/_DEVPROP_FILTER_EXPRESSION
 - PDEVPROP_FILTER_EXPRESSION
 - devfiltertypes/PDEVPROP_FILTER_EXPRESSION
 - DEVPROP_FILTER_EXPRESSION
 - devfiltertypes/DEVPROP_FILTER_EXPRESSION
dev_langs:
 - c++
helpviewer_keywords:
 - _DEVPROP_FILTER_EXPRESSION
---

## -description

Describes a filter expression used to query filter results.

## -struct-fields

### -field Operator

A [DEVPROP_OPERATOR](ne-devfiltertypes-devprop_operator.md) value describing the operator for this filter expression element.

### -field Property

The [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) structure that should be associated with the filter operation described by the *Operator* member

## -remarks

**DEVPROP_FILTER_EXPRESSION** structures can be combined in an array to create a complex filter expression for use in query creation, such as through the [DevCreateObjectQuery](../devquery/nf-devquery-devcreateobjectquery.md) function.

The following example demonstrates the initialization of a **DEVPROP_FILTER_EXPRESSION**.

```cpp
ULONG targetValue = 5;
DEVPROP_BOOLEAN devpropTrue = DEVPROP_TRUE;
const DEVPROP_FILTER_EXPRESSION filter[] = {
    {DEVPROP_OPERATOR_OR_OPEN, {0}},
        {DEVPROP_OPERATOR_EQUALS, {{DEVPKEY_Property1, DEVPROP_STORE_SYSTEM, NULL}, DEVPROP_TYPE_UINT32, (ULONG)(sizeof(targetValue)), (PVOID)&targetValue}},
        {DEVPROP_OPERATOR_EQUALS, {{DEVPKEY_Property2, DEVPROP_STORE_SYSTEM, NULL}, DEVPROP_TYPE_BOOLEAN, (ULONG)(sizeof(devpropTrue)), (PVOID)&devpropTrue}},
    {DEVPROP_OPERATOR_OR_CLOSE, {0}}
};

```

If the above filter expression was used in a query, the query’s result set would consist of all objects of the appropriate type that have a *DEVPKEY_Property1* property equal to 5 OR that have a *DEVPKEY_Property2* property equal to **DEVPROP_TRUE**. 

If a filter expression does not contain any logical operators specifying how to combine different comparison clauses, then the filter expression assumes that a logical AND should be performed.


## -see-also

