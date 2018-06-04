---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_wmiutils_0000_0001_0002 enumeration


## -description


Contains flags that describe query tokens used in the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a> method. 


## -enum-fields




### -field WMIQ_RPN_TOKEN_EXPRESSION

This token is an expression, for example, J = 7.


### -field WMIQ_RPN_TOKEN_AND

This token is a logical AND.


### -field WMIQ_RPN_TOKEN_OR

This token is a logical OR.


### -field WMIQ_RPN_TOKEN_NOT

This token is a logical NOT.


### -field WMIQ_RPN_OP_UNDEFINED

The operator is undefined or unknown.


### -field WMIQ_RPN_OP_EQ

The operator is  equal-to  (=).


### -field WMIQ_RPN_OP_NE

The operator is  not-equal-to  (&lt;&gt;).


### -field WMIQ_RPN_OP_GE

The operator is  greater-than-or-equal-to  (&gt;=).


### -field WMIQ_RPN_OP_LE

The operator is  less-than-or-equal-to  (&lt;=).


### -field WMIQ_RPN_OP_LT

The operator is  less-than (&lt;) .


### -field WMIQ_RPN_OP_GT

The operator is  greater-than  (&gt;).


### -field WMIQ_RPN_OP_LIKE

The operator is  LIKE.


### -field WMIQ_RPN_OP_ISA

The operator is  ISA.


### -field WMIQ_RPN_OP_ISNOTA

The operator is  ISNOTA.


### -field WMIQ_RPN_OP_ISNULL

The operator is  ISNULL.


### -field WMIQ_RPN_OP_ISNOTNULL

The operator is  ISNOTNULL.


### -field WMIQ_RPN_LEFT_PROPERTY_NAME

Left argument is a property name.


### -field WMIQ_RPN_RIGHT_PROPERTY_NAME

Right argument is a property name.


### -field WMIQ_RPN_CONST2

Has a second constant. Used with "BETWEEN" clauses.


### -field WMIQ_RPN_CONST

Has a constant.


### -field WMIQ_RPN_RELOP

The field <b>m_uOperator</b> is not 0 (zero).


### -field WMIQ_RPN_LEFT_FUNCTION

Left argument is a function.


### -field WMIQ_RPN_RIGHT_FUNCTION

Right argument is a function.


### -field WMIQ_RPN_GET_TOKEN_TYPE

Reserved for future use.


### -field WMIQ_RPN_GET_EXPR_SHAPE

Reserved for future use.


### -field WMIQ_RPN_GET_LEFT_FUNCTION

Reserved for future use.


### -field WMIQ_RPN_GET_RIGHT_FUNCTION

Reserved for future use.


### -field WMIQ_RPN_GET_RELOP

Reserved for future use.


### -field WMIQ_RPN_NEXT_TOKEN

Reserved for future use.


### -field WMIQ_RPN_FROM_UNARY

FROM clause contains a single class.


### -field WMIQ_RPN_FROM_PATH

FROM clause contains an object path.


### -field WMIQ_RPN_FROM_CLASS_LIST

FROM clause contains a list of classes.


### -field WMIQ_RPN_FROM_MULTIPLE

Reserved for future use.

