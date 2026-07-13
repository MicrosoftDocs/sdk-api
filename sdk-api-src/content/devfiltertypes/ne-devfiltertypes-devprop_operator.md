---
UID: NE:devfiltertypes._DEVPROP_OPERATOR
tech.root: devinst
title: DEVPROP_OPERATOR
ms.date: 11/04/2024
targetos: Windows
description: Specifies the operations that can be used for a DEVPROP_FILTER_EXPRESSION.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: devfiltertypes.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devfiltertypes.h
api_name:
 - _DEVPROP_OPERATOR
 - PDEVPROP_OPERATOR
 - DEVPROP_OPERATOR
f1_keywords:
 - _DEVPROP_OPERATOR
 - devfiltertypes/_DEVPROP_OPERATOR
 - PDEVPROP_OPERATOR
 - devfiltertypes/PDEVPROP_OPERATOR
 - DEVPROP_OPERATOR
 - devfiltertypes/DEVPROP_OPERATOR
dev_langs:
 - c++
helpviewer_keywords:
 - _DEVPROP_OPERATOR
---

## -description

Specifies the operations that can be used for a [DEVPROP_FILTER_EXPRESSION](ns-devfiltertypes-devprop_filter_expression.md)

## -enum-fields

### -field DEVPROP_OPERATOR_MODIFIER_NOT

Used in conjunction with a comparison operator and negates the comparison.

### -field DEVPROP_OPERATOR_MODIFIER_IGNORE_CASE

Used in conjunction with a comparison operator when evaluating a string and causes the comparison to ignore the case of the string.

### -field DEVPROP_OPERATOR_NONE

Not a valid operator.

### -field DEVPROP_OPERATOR_EXISTS

A comparison operator that evaluates to true if the associated property exists and false otherwise.

### -field DEVPROP_OPERATOR_NOT_EXISTS

A comparison operator that evaluates to true if the associated property does not exist and false otherwise.

### -field DEVPROP_OPERATOR_EQUALS

A comparison operator that evaluates to true if the associated property is equal to the specified value.

### -field DEVPROP_OPERATOR_NOT_EQUALS

A comparison operator that evaluates to true if the associated property is not equal to the specified value.

### -field DEVPROP_OPERATOR_GREATER_THAN

Only valid with numeric property types. A comparison operator that evaluates to true if the value of the associated property is greater than the specified value.

### -field DEVPROP_OPERATOR_LESS_THAN

Only valid with numeric property types. A comparison operator that evaluates to true if the value of the associated property is less than the specified value.

### -field DEVPROP_OPERATOR_GREATER_THAN_EQUALS

Only valid with numeric property types. A comparison operator that evaluates to true if the value of the associated property is greater than or equal to the specified value.

### -field DEVPROP_OPERATOR_LESS_THAN_EQUALS

Only valid with numeric property types. A comparison operator that evaluates to true if the value of the associated property is less than or equal to the specified value.

### -field DEVPROP_OPERATOR_EQUALS_IGNORE_CASE

Only valid with string property types. A comparison operator that compares if two strings are equal, ignoring casing.

### -field DEVPROP_OPERATOR_NOT_EQUALS_IGNORE_CASE

Only valid with string property types. A comparison operator that compares if two strings are not equal, ignoring casing.

### -field DEVPROP_OPERATOR_BITWISE_AND

Only valid with property type DEVPROP_TYPE_UINT32. A comparison operator that performs a bitwise AND operation between the value of the associated property and the specified value and returns true if the result is not 0.

### -field DEVPROP_OPERATOR_BITWISE_OR

Only valid with property type DEVPROP_TYPE_UINT32. A comparison operator that performs a bitwise OR operation between the value of the associated property and the specified value and returns true if the result is not 0.

### -field DEVPROP_OPERATOR_BEGINS_WITH

Only valid with string property types. A comparison operator that returns true if the value of the associated property starts with the specified string. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_ENDS_WITH

Only valid with string property types. A comparison operator that returns true if the value of the associated property ends with the specified string. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_CONTAINS

Only valid with string property types. A comparison operator that returns true if the value of the associated property contains the specified string. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_BEGINS_WITH_IGNORE_CASE

Only valid with string property types. A comparison operator that returns true if the value of the associated property ends with the specified string. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_ENDS_WITH_IGNORE_CASE

Only valid with string property types. A comparison operator that returns true if the value of the associated property ends with the specified string. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_CONTAINS_IGNORE_CASE

Only valid with string property types. A comparison operator that returns true if the value of the associated property contains the specified string. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_LIST_CONTAINS

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that matches the specified value. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_BEGINS_WITH

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that begins with the specified value. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_ENDS_WITH

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that ends with the specified value. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_CONTAINS

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that matches the specified value. This performs a case sensitive comparison.

### -field DEVPROP_OPERATOR_LIST_CONTAINS_IGNORE_CASE

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that matches the specified value. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_BEGINS_WITH_IGNORE_CASE

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that begins with the specified value. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_ENDS_WITH_IGNORE_CASE

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that ends with the specified value. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_LIST_ELEMENT_CONTAINS_IGNORE_CASE

Only valid with property type DEVPROP_TYPE_STRING_LIST. A comparison operator that returns true if the value of the associated property has an element that matches the specified value. This performs a case insensitive comparison.

### -field DEVPROP_OPERATOR_AND_OPEN

Logical operator that is used on its own without an associated property. It starts a new clause where sub clauses are evaluated using AND logic.

### -field DEVPROP_OPERATOR_AND_CLOSE

Logical operator that is used on its own without an associated property. It ends a clause opened with DEVPROP_OPERATOR_AND_OPEN.

### -field DEVPROP_OPERATOR_OR_OPEN

Logical operator that is used on its own without an associated property. It starts a new clause where sub clauses are evaluated using OR logic.

### -field DEVPROP_OPERATOR_OR_CLOSE

Logical operator that is used on its own without an associated property. It ends a clause opened with DEVPROP_OPERATOR_OR_OPEN.

### -field DEVPROP_OPERATOR_NOT_OPEN

Logical operator that is used on its own without an associated property. It starts a new clause where sub clauses are evaluated and the result is negated.

### -field DEVPROP_OPERATOR_NOT_CLOSE

Logical operator that is used on its own without an associated property. It ends a clause opened with DEVPROP_OPERATOR_NOT_OPEN.

### -field DEVPROP_OPERATOR_ARRAY_CONTAINS

Only valid with property types that are arrays (DEVPROP_TYPEMOD_ARRAY).  A comparison operator that returns true if the value of the associated property contains an array element that matches the specified value.

### -field DEVPROP_OPERATOR_MASK_EVAL

Not a valid operator in a filter expression.  This is used to retrieve the comparison operator part of a DEVPROP_OPERATOR.

### -field DEVPROP_OPERATOR_MASK_LIST

Not a valid operator in a filter expression.  This is used to retrieve the list operator part of a DEVPROP_OPERATOR.

### -field DEVPROP_OPERATOR_MASK_MODIFIER

Not a valid operator in a filter expression.  This is used to retrieve the operator modifier part of a DEVPROP_OPERATOR.

### -field DEVPROP_OPERATOR_MASK_NOT_LOGICAL

Not a valid operator in a filter expression.  This is used to retrieve the parts of a DEVPROP_OPERATOR that are not the logical operator part.

### -field DEVPROP_OPERATOR_MASK_LOGICAL

Not a valid operator in a filter expression.  This is used to retrieve the parts of a DEVPROP_OPERATOR that are the logical operator part.

### -field DEVPROP_OPERATOR_MASK_ARRAY

Not a valid operator in a filter expression.  This is used to retrieve the array operator part of a DEVPROP_OPERATOR.

## -remarks

## -see-also

