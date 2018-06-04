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

# tag_SWbemQueryQualifiedName structure


## -description


The <b>SWbemQueryQualifiedName</b> structure stores property names for the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a> method.


## -struct-fields




### -field m_uVersion

Unused. Always 1 (one).


### -field m_uTokenType

Unused. Always 1 (one).


### -field m_uNameListSize

Number of elements in the list of names. For example, for the  "propName" property,  <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".


### -field m_ppszNameList

List of property names. For example, for the  "propName" property, <b>m_uNameListSize</b> is 1 (one) and <b>m_ppszNameList</b> is "propName".


### -field m_bArraysUsed

Unused. Always <b>false</b>.


### -field m_pbArrayElUsed

Unused. Always <b>NULL</b>.


### -field m_puArrayIndex

Unused. Always <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/4a0c0c1d-3d84-491f-8379-d164821fa71b">IWbemQuery</a>



<a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">IWbemQuery::GetAnalysis</a>



<a href="https://msdn.microsoft.com/0f7e77a8-4ee6-421b-be4a-b58055a58c39">SWbemRpnEncodedQuery</a>
 

 

