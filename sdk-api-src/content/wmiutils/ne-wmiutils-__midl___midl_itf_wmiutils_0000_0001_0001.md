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

# __MIDL___MIDL_itf_wmiutils_0000_0001_0001 enumeration


## -description


Contains constants used to specify the type of analysis to perform by using the <a href="https://msdn.microsoft.com/06cd2593-58f5-46b9-9100-debad0280d90">GetAnalysis</a> method.


## -enum-fields




### -field WMIQ_ANALYSIS_RPN_SEQUENCE

Used if the query has a SELECT clause. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="https://msdn.microsoft.com/0f7e77a8-4ee6-421b-be4a-b58055a58c39">SWbemRpnEncodedQuery</a> structure.


### -field WMIQ_ANALYSIS_ASSOC_QUERY

Used to return information about association type queries. When this type of analysis is used,  <i>pAnalysis</i> points to an <a href="https://msdn.microsoft.com/8312b324-a698-4957-bd76-3129398e4886">SWbemAssocQueryInf</a> structure.


### -field WMIQ_ANALYSIS_PROP_ANALYSIS_MATRIX

Unused.  Reserved for future use.


### -field WMIQ_ANALYSIS_QUERY_TEXT

Used to return a text string that has the original query text. If this type of analysis is used,  <i>pAnalysis</i> points to a text string that contains the original query text.

You can use this parameter if  a parser object is passed to another method.


### -field WMIQ_ANALYSIS_RESERVED

Unused.  Reserved for future use.

