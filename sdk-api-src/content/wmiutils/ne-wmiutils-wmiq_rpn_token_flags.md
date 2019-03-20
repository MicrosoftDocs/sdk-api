---
UID: NE:wmiutils.__MIDL___MIDL_itf_wmiutils_0000_0001_0002
title: WMIQ_RPN_TOKEN_FLAGS (wmiutils.h)
author: windows-sdk-content
description: Contains flags that describe query tokens used in the GetAnalysis method.
old-location: wmi\wmiq_rpn_token_flags.htm
tech.root: WmiSdk
ms.assetid: fe6d6931-73b2-43d0-a703-a1a58770f4a0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMIQ_RPN_CONST, WMIQ_RPN_CONST2, WMIQ_RPN_FROM_CLASS_LIST, WMIQ_RPN_FROM_MULTIPLE, WMIQ_RPN_FROM_PATH, WMIQ_RPN_FROM_UNARY, WMIQ_RPN_GET_EXPR_SHAPE, WMIQ_RPN_GET_LEFT_FUNCTION, WMIQ_RPN_GET_RELOP, WMIQ_RPN_GET_RIGHT_FUNCTION, WMIQ_RPN_GET_TOKEN_TYPE, WMIQ_RPN_LEFT_FUNCTION, WMIQ_RPN_LEFT_PROPERTY_NAME, WMIQ_RPN_NEXT_TOKEN, WMIQ_RPN_OP_EQ, WMIQ_RPN_OP_GE, WMIQ_RPN_OP_GT, WMIQ_RPN_OP_ISA, WMIQ_RPN_OP_ISNOTA, WMIQ_RPN_OP_ISNOTNULL, WMIQ_RPN_OP_ISNULL, WMIQ_RPN_OP_LE, WMIQ_RPN_OP_LIKE, WMIQ_RPN_OP_LT, WMIQ_RPN_OP_NE, WMIQ_RPN_OP_UNDEFINED, WMIQ_RPN_RELOP, WMIQ_RPN_RIGHT_FUNCTION, WMIQ_RPN_RIGHT_PROPERTY_NAME, WMIQ_RPN_TOKEN_AND, WMIQ_RPN_TOKEN_EXPRESSION, WMIQ_RPN_TOKEN_FLAGS, WMIQ_RPN_TOKEN_FLAGS enumeration [Windows Management Instrumentation], WMIQ_RPN_TOKEN_NOT, WMIQ_RPN_TOKEN_OR, wmi.wmiq_rpn_token_flags, wmiutils/WMIQ_RPN_CONST, wmiutils/WMIQ_RPN_CONST2, wmiutils/WMIQ_RPN_FROM_CLASS_LIST, wmiutils/WMIQ_RPN_FROM_MULTIPLE, wmiutils/WMIQ_RPN_FROM_PATH, wmiutils/WMIQ_RPN_FROM_UNARY, wmiutils/WMIQ_RPN_GET_EXPR_SHAPE, wmiutils/WMIQ_RPN_GET_LEFT_FUNCTION, wmiutils/WMIQ_RPN_GET_RELOP, wmiutils/WMIQ_RPN_GET_RIGHT_FUNCTION, wmiutils/WMIQ_RPN_GET_TOKEN_TYPE, wmiutils/WMIQ_RPN_LEFT_FUNCTION, wmiutils/WMIQ_RPN_LEFT_PROPERTY_NAME, wmiutils/WMIQ_RPN_NEXT_TOKEN, wmiutils/WMIQ_RPN_OP_EQ, wmiutils/WMIQ_RPN_OP_GE, wmiutils/WMIQ_RPN_OP_GT, wmiutils/WMIQ_RPN_OP_ISA, wmiutils/WMIQ_RPN_OP_ISNOTA, wmiutils/WMIQ_RPN_OP_ISNOTNULL, wmiutils/WMIQ_RPN_OP_ISNULL, wmiutils/WMIQ_RPN_OP_LE, wmiutils/WMIQ_RPN_OP_LIKE, wmiutils/WMIQ_RPN_OP_LT, wmiutils/WMIQ_RPN_OP_NE, wmiutils/WMIQ_RPN_OP_UNDEFINED, wmiutils/WMIQ_RPN_RELOP, wmiutils/WMIQ_RPN_RIGHT_FUNCTION, wmiutils/WMIQ_RPN_RIGHT_PROPERTY_NAME, wmiutils/WMIQ_RPN_TOKEN_AND, wmiutils/WMIQ_RPN_TOKEN_EXPRESSION, wmiutils/WMIQ_RPN_TOKEN_FLAGS, wmiutils/WMIQ_RPN_TOKEN_NOT, wmiutils/WMIQ_RPN_TOKEN_OR
ms.topic: enum
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WMIUtils.h
api_name:
 - WMIQ_RPN_TOKEN_FLAGS
product: Windows
targetos: Windows
req.typenames: WMIQ_RPN_TOKEN_FLAGS
req.redist: 
---

# WMIQ_RPN_TOKEN_FLAGS enumeration


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

