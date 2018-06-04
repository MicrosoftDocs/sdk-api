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
 

 

