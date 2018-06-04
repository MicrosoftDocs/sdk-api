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

# IDvbContentDescriptor::GetRecordContentNibbles


## -description


Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">IDvbContentDescriptor::GetCountOfRecords</a>



### -param pbValLevel1 [out]

Gets the most-significant four bits of the content identifier.


### -param pbValLevel2 [out]

Gets the least-significant four bits of the content identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of content descriptors associated with the values returned in the <i>dwVal1</i> and <i>dwVal2</i> parameters, see Table 28 in Section 6.2.9 of the DVB standard document titled  
      <i>Digital Video Broadcasting (DVB);
Specification for Service Information (SI) in DVB systems (DVB Document A038 Rev. 4)</i>. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/7bc74428-f8e3-4d3b-b35a-33e917b18a93">IDvbContentDescriptor</a>
 

 

