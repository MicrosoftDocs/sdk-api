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

# __MIDL___MIDL_itf_msrdc_0000_0000_0013 structure


## -description


Contains the file index information that the <a href="https://msdn.microsoft.com/09c9b918-1def-4d19-84d4-99b881070e36">ISimilarityTraitsTable::FindSimilarFileIndex</a> method returned for a matching file.


## -struct-fields




### -field m_FileIndex

The index of the matching file in the similarity traits table.


### -field m_MatchCount

The number of traits that were matched. The valid range is from <b>MSRDC_MINIMUM_MATCHESREQUIRED</b> to 
      <b>MSRDC_MAXIMUM_MATCHESREQUIRED</b>.


## -see-also




<a href="https://msdn.microsoft.com/09c9b918-1def-4d19-84d4-99b881070e36">ISimilarityTraitsTable::FindSimilarFileIndex</a>
 

 

