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

# IDvbTeletextDescriptor::GetRecordMagazineNumber


## -description



  Gets the magazine number from a Digital Video Broadcast (DVB) teletext descriptor.
  A <i>magazine</i> is a sequence of one or more pages in an enhanced-teletext packet that are normally repeatedly transmitted in numerical sequence


## -parameters




### -param bRecordIndex [in]


  Zero-based index of the descriptor to return. To get the number of descriptors, call 
  <a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">
  IDvbTeletextDescriptor::GetCountOfRecords
</a>.



### -param pbVal [out]

Receives the magazine number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5148a87b-e6b6-4bda-871c-10a2f398ebcc">IDvbTeletextDescriptor</a>



<a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">
  IDvbTeletextDescriptor::GetCountOfRecords
</a>
 

 

