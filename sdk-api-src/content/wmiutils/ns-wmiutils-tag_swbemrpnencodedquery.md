---
UID: NS:wmiutils.tag_SWbemRpnEncodedQuery
title: tag_SWbemRpnEncodedQuery
author: windows-sdk-content
description: The SWbemRpnEncodedQuery structure contains information from the IWbemQuery::GetAnalysis method when you use the WMIQ_ANALYSIS_RPN_SEQUENCE analysis type. Not all the fields in the structure are used actively, because some are reserved for future use.
old-location: wmi\swbemrpnencodedquery.htm
old-project: WmiSdk
ms.assetid: 0f7e77a8-4ee6-421b-be4a-b58055a58c39
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: SWbemRpnEncodedQuery, SWbemRpnEncodedQuery structure [Windows Management Instrumentation], WMIQ_RPN_FROM_CLASS_LIST, WMIQ_RPN_FROM_PATH, WMIQ_RPN_FROM_UNARY, tag_SWbemRpnEncodedQuery, wmi.swbemrpnencodedquery, wmiutils/SWbemRpnEncodedQuery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SWbemRpnEncodedQuery
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmiutils.h
api_name:
-	SWbemRpnEncodedQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tag_SWbemRpnEncodedQuery structure


## -description


The <b>SWbemRpnEncodedQuery</b> structure contains information from the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a> method when you use the <b>WMIQ_ANALYSIS_RPN_SEQUENCE</b> analysis type. Not all  the fields in the structure are used actively, because some are reserved for future use.


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

Structure used to store property names. This field is used  with the  <b>m_uSelectListSize</b> field. For example, in the statement <code>SELECT a,b,c FROM d</code>, <b>m_uSelectListSize</b> is 3, and the <b>m_ppszNameList</b> field of the <b>m_ppSelectList</b> structure contains the strings "a", "b" and "c". For more information, see <a href="https://msdn.microsoft.com/ce8031a1-b30f-4ff6-90d8-42e46e1b6d89">SWbemQueryQualifiedName</a>.


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

<a href="https://msdn.microsoft.com/04ef89e5-ce42-4d2d-8188-c2bbfe821bcc">SWbemRpnQueryToken</a>
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




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>



<a href="https://msdn.microsoft.com/ce8031a1-b30f-4ff6-90d8-42e46e1b6d89">SWbemQueryQualifiedName</a>



<a href="https://msdn.microsoft.com/04ef89e5-ce42-4d2d-8188-c2bbfe821bcc">SWbemRpnQueryToken</a>
 

 

