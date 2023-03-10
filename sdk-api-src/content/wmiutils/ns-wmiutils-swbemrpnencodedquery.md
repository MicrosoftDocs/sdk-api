---
UID: NS:wmiutils.tag_SWbemRpnEncodedQuery
title: SWbemRpnEncodedQuery (wmiutils.h)
description: The SWbemRpnEncodedQuery structure contains information from the IWbemQuery::GetAnalysis method when you use the WMIQ_ANALYSIS_RPN_SEQUENCE analysis type. Not all the fields in the structure are used actively, because some are reserved for future use.
helpviewer_keywords: ["SWbemRpnEncodedQuery","SWbemRpnEncodedQuery structure [Windows Management Instrumentation]","WMIQ_RPN_FROM_CLASS_LIST","WMIQ_RPN_FROM_PATH","WMIQ_RPN_FROM_UNARY","wmi.swbemrpnencodedquery","wmiutils/SWbemRpnEncodedQuery"]
old-location: wmi\swbemrpnencodedquery.htm
tech.root: wmi
ms.assetid: 0f7e77a8-4ee6-421b-be4a-b58055a58c39
ms.date: 12/05/2018
ms.keywords: SWbemRpnEncodedQuery, SWbemRpnEncodedQuery structure [Windows Management Instrumentation], WMIQ_RPN_FROM_CLASS_LIST, WMIQ_RPN_FROM_PATH, WMIQ_RPN_FROM_UNARY, wmi.swbemrpnencodedquery, wmiutils/SWbemRpnEncodedQuery
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
req.typenames: SWbemRpnEncodedQuery
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_SWbemRpnEncodedQuery
 - wmiutils/tag_SWbemRpnEncodedQuery
 - SWbemRpnEncodedQuery
 - wmiutils/SWbemRpnEncodedQuery
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
 - SWbemRpnEncodedQuery
---

# SWbemRpnEncodedQuery structure


## -description

The <b>SWbemRpnEncodedQuery</b> structure contains information from the <a href="/windows/desktop/api/wmiutils/nf-wmiutils-iwbemquery-getanalysis">IWbemQuery::GetAnalysis</a> method when you use the <b>WMIQ_ANALYSIS_RPN_SEQUENCE</b> analysis type. Not all  the fields in the structure are used actively, because some are reserved for future use.

## -struct-fields

### -field m_uVersion

Unused.  Value is always 1.

### -field m_uTokenType

Unused.  Value is always 0 (zero).

### -field m_uParsedFeatureMask

Unused.  Value is always 0 (zero).

### -field m_uDetectedArraySize

Unused. Value is always 0 (zero).

### -field m_puDetectedFeatures

Unused. Value is always <b>NULL</b>.

### -field m_uSelectListSize

Number of elements listed in a SELECT clause. For example, in the statement <code>SELECT a,b,c FROM d</code>, <b>m_uSelectListSize</b> is the value 3 (a, b and c).

### -field m_ppSelectList

Structure used to store property names. This field is used  with the  <b>m_uSelectListSize</b> field. For example, in the statement <code>SELECT a,b,c FROM d</code>, <b>m_uSelectListSize</b> is 3, and the <b>m_ppszNameList</b> field of the <b>m_ppSelectList</b> structure contains the strings "a", "b" and "c". For more information, see <a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemqueryqualifiedname">SWbemQueryQualifiedName</a>.

### -field m_uFromTargetType

Bitmap used to indicate  the form of the FROM clause.



#### WMIQ_RPN_FROM_UNARY (1 (0x1))

FROM clause contains a single class.



#### WMIQ_RPN_FROM_PATH (2 (0x2))

FROM clause contains an object path.



#### WMIQ_RPN_FROM_CLASS_LIST (4 (0x4))

FROM clause contains a list of classes.

### -field m_pszOptionalFromPath

Optional FROM path. If not used this field is <b>NULL</b>.

### -field m_uFromListSize

Number of items in the FROM clause of the SELECT statement.  For example, in the statement, <code>SELECT * FROM  a, b</code>, the value of <b>m_uFromListSize</b> is 2.

### -field m_ppszFromList

Pointer to a list of strings. Each string is one element of the FROM clause of a SELECT statement.  For example, in the statement <code>SELECT * FROM a, b</code>, the list  contains the strings "a" and "b".

### -field m_uWhereClauseSize

Number of tokens in the WHERE clause. For example, in the statement <code>SELECT  * FROM a, b WHERE c &lt; 1000 AND d ISA e</code>, the value of <b>m_uWhereClauseSize</b> is 2 (the phrases <code>c &lt; 1000</code> and <code>d ISA e</code>).

### -field m_ppRpnWhereClause

<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnquerytoken">SWbemRpnQueryToken</a>
<code>SELECT * FROM a, b WHERE c &lt; 1000 AND d ISA e</code>
<code>c &lt; 1000</code>
<code>d ISA e</code>
<code>AND</code>

### -field m_dblWithinPolling

If there is a WITHIN clause, this field indicates the polling interval. If there is a GROUP WITHIN  clause, this <b>m_dblWithinPolling</b> is unused.

### -field m_dblWithinWindow

Used if there is  a GROUP WITHIN clause to indicate the interval over which to group results.

### -field m_uOrderByListSize

### -field m_ppszOrderByList

### -field m_uOrderDirectionEl

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbemquery">IWbemQuery</a>



<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemqueryqualifiedname">SWbemQueryQualifiedName</a>



<a href="/windows/win32/api/wmiutils/ns-wmiutils-swbemrpnquerytoken">SWbemRpnQueryToken</a>