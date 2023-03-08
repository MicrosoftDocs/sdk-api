---
UID: NS:wmiutils.tag_SWbemRpnQueryToken
title: SWbemRpnQueryToken (wmiutils.h)
description: The SWbemRpnQueryToken structure represents the query tokens in a WMIQ_ANALYSIS_RPN_SEQUENCE type query. An example of a query token is the following:\_j &gt; 4.
helpviewer_keywords: ["SWbemRpnQueryToken","SWbemRpnQueryToken structure [Windows Management Instrumentation]","VT_BOOL","VT_I4","VT_I8","VT_LPWSTR","VT_R8","VT_UI4","VT_UI8","WMIQ_RPN_CONST","WMIQ_RPN_CONST2","WMIQ_RPN_LEFT_FUNCTION","WMIQ_RPN_LEFT_PROPERTY_NAME","WMIQ_RPN_OP_EQ","WMIQ_RPN_OP_GE","WMIQ_RPN_OP_GT","WMIQ_RPN_OP_ISA","WMIQ_RPN_OP_ISNOTA","WMIQ_RPN_OP_ISNOTNULL","WMIQ_RPN_OP_ISNULL","WMIQ_RPN_OP_LE","WMIQ_RPN_OP_LIKE","WMIQ_RPN_OP_LT","WMIQ_RPN_OP_NE","WMIQ_RPN_OP_UNDEFINED","WMIQ_RPN_RELOP","WMIQ_RPN_RIGHT_FUNCTION","WMIQ_RPN_RIGHT_PROPERTY_NAME","WMIQ_RPN_TOKEN_AND","WMIQ_RPN_TOKEN_EXPRESSION","WMIQ_RPN_TOKEN_NOT","WMIQ_RPN_TOKEN_OR","wmi.swbemrpnquerytoken","wmiutils/SWbemRpnQueryToken"]
old-location: wmi\swbemrpnquerytoken.htm
tech.root: wmi
ms.assetid: 04ef89e5-ce42-4d2d-8188-c2bbfe821bcc
ms.date: 12/05/2018
ms.keywords: SWbemRpnQueryToken, SWbemRpnQueryToken structure [Windows Management Instrumentation], VT_BOOL, VT_I4, VT_I8, VT_LPWSTR, VT_R8, VT_UI4, VT_UI8, WMIQ_RPN_CONST, WMIQ_RPN_CONST2, WMIQ_RPN_LEFT_FUNCTION, WMIQ_RPN_LEFT_PROPERTY_NAME, WMIQ_RPN_OP_EQ, WMIQ_RPN_OP_GE, WMIQ_RPN_OP_GT, WMIQ_RPN_OP_ISA, WMIQ_RPN_OP_ISNOTA, WMIQ_RPN_OP_ISNOTNULL, WMIQ_RPN_OP_ISNULL, WMIQ_RPN_OP_LE, WMIQ_RPN_OP_LIKE, WMIQ_RPN_OP_LT, WMIQ_RPN_OP_NE, WMIQ_RPN_OP_UNDEFINED, WMIQ_RPN_RELOP, WMIQ_RPN_RIGHT_FUNCTION, WMIQ_RPN_RIGHT_PROPERTY_NAME, WMIQ_RPN_TOKEN_AND, WMIQ_RPN_TOKEN_EXPRESSION, WMIQ_RPN_TOKEN_NOT, WMIQ_RPN_TOKEN_OR, wmi.swbemrpnquerytoken, wmiutils/SWbemRpnQueryToken
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
targetos: Windows
req.typenames: SWbemRpnQueryToken
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_SWbemRpnQueryToken
 - wmiutils/tag_SWbemRpnQueryToken
 - SWbemRpnQueryToken
 - wmiutils/SWbemRpnQueryToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmiutils.h
api_name:
 - SWbemRpnQueryToken
---

# SWbemRpnQueryToken structure


## -description

The <b>SWbemRpnQueryToken</b> structure represents the query tokens in a WMIQ_ANALYSIS_RPN_SEQUENCE type query. An example of a query token is the following:  j &gt; 4.

## -struct-fields

### -field m_uVersion

Unused. Always 1.

### -field m_uTokenType

Type of token this instance represents.



#### WMIQ_RPN_TOKEN_EXPRESSION (1)

This token is an expression, for example, J = 7.



#### WMIQ_RPN_TOKEN_AND (2)

This token is a logical AND.



#### WMIQ_RPN_TOKEN_OR (3)

This token is a logical OR.



#### WMIQ_RPN_TOKEN_NOT (4)

This token is a logical NOT.

### -field m_uSubexpressionShape

If the <b>m_uTokenType</b> member is <b>WMIQ_RPN_TOKEN_EXPRESSION</b>, <b>m_uSubexpressionShape</b> bitmask value specifies the shape of the expression.



#### WMIQ_RPN_LEFT_PROPERTY_NAME (1 (0x1))

Left argument is a property name.



#### WMIQ_RPN_RIGHT_PROPERTY_NAME (2 (0x2))

Right argument is a property name.



#### WMIQ_RPN_CONST2 (4 (0x4))

Has a second constant. Used with "BETWEEN" clauses.



#### WMIQ_RPN_CONST (8 (0x8))

Has a constant.



#### WMIQ_RPN_RELOP (16 (0x10))

The field <b>m_uOperator</b> is not 0 (zero).



#### WMIQ_RPN_LEFT_FUNCTION (32 (0x20))

Left argument is a function.



#### WMIQ_RPN_RIGHT_FUNCTION (64 (0x40))

Right argument is a function.

### -field m_uOperator

This field can have the value 0 (zero), or one of the following values.



#### WMIQ_RPN_OP_UNDEFINED (0 (0x0))

The operator is undefined or unknown.



#### WMIQ_RPN_OP_EQ (1 (0x1))

The operator is  equal-to  (=).



#### WMIQ_RPN_OP_NE (2 (0x2))

The operator is  not-equal-to  (&lt;&gt;).



#### WMIQ_RPN_OP_GE (3 (0x3))

The operator is  greater-than-or-equal-to  (&gt;=).



#### WMIQ_RPN_OP_LE (4 (0x4))

The operator is  less-than-or-equal-to  (&lt;=).



#### WMIQ_RPN_OP_LT (5 (0x5))

The operator is  less-than (&lt;) .



#### WMIQ_RPN_OP_GT (6 (0x6))

The operator is  greater-than  (&gt;).



#### WMIQ_RPN_OP_LIKE (7 (0x7))

The operator is  LIKE.



#### WMIQ_RPN_OP_ISA (8 (0x8))

The operator is  ISA.



#### WMIQ_RPN_OP_ISNOTA (9 (0x9))

The operator is  ISNOTA.



#### WMIQ_RPN_OP_ISNULL (10 (0xA))

The operator is  ISNULL.



#### WMIQ_RPN_OP_ISNOTNULL (11 (0xB))

The operator is  ISNOTNULL.

### -field m_pRightIdent

If there are two property names in a token, <b>m_pRightIdent</b> is used to identify the right property name.

### -field m_pLeftIdent

If there are two property names in a token <b>m_pLeftIdent</b> is used to identify the left property name. If only one property name is present, it appears in this member.

### -field m_uConstApparentType

Apparent data type of the constant.



#### VT_I4 (3 (0x3))

Long data type.



#### VT_R8 (5 (0x5))

Double precision floating-point data type.



#### VT_BOOL (11 (0xB))

Boolean data type



#### VT_UI4 (19 (0x13))

Unsigned long data type.



#### VT_I8 (20 (0x14))

Signed 64-bit integer.



#### VT_UI8 (21 (0x15))

Unsigned 64-bit integer.



#### VT_LPWSTR (31 (0x1F))

LPCWSTR data type.

### -field m_Const

Value of the first constant. For more information, see <a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnquerytoken">SWbemRpnConst</a>.

### -field m_uConst2ApparentType

Type of second constant.  The fields <b>m_uConst2ApparentType</b> and <b>m_uConst2</b> are used only for BETWEEN phrases.



#### VT_I4 (3 (0x3))

Long data type.



#### VT_R8 (5 (0x5))

Double precision floating-point data type.



#### VT_BOOL (11 (0xB))

Boolean data type.



#### VT_UI4 (19 (0x13))

Unsigned long data type.



#### VT_I8 (20 (0x14))

Signed 64-bit integer.



#### VT_UI8 (21 (0x15))

Unsigned 64-bit integer.



#### VT_LPWSTR (31 (0x1F))

LPCWSTR data type.

### -field m_Const2

Value of the second constant. The fields <b>m_uConst2ApparentType</b> and <b>m_uConst2</b> are used only for BETWEEN phrases. For more information, see <a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnquerytoken">SWbemRpnConst</a>.

### -field m_pszRightFunc

Specifies a function on the right of the operator in a WHERE clause. If there is no function on the right of the operator in this token, this field is <b>NULL</b>.

### -field m_pszLeftFunc

Specifies a function on the left of the operator in a WHERE clause. If there is no function on the left of the operator in this token, this field is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>



<a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a>



<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnquerytoken">SWbemRpnConst</a>



<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnencodedquery">SWbemrpnEncodedQuery</a>