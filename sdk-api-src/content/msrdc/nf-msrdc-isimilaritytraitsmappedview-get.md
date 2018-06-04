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

# ISimilarityTraitsMappedView::Get


## -description


Returns information about the mapped view of a similarity traits table file.


## -parameters




### -param index




### -param dirty [in]

If <b>TRUE</b> is specified, the data in the currently mapped view has been changed; otherwise, the data has not changed. This parameter can be used to determine if data may need to be written to disk.


### -param numElements [in]

Minimum number of bytes of data to be mapped in the mapped view.


### -param viewInfo [out]

Pointer to a location that receives a <a href="https://msdn.microsoft.com/f7bd0ebd-6abd-4d2c-af7d-21a90a633276">SimilarityMappedViewInfo</a> structure containing information about the mapped view.


#### - fileOffset [in]

Beginning file offset, in bytes, of the underlying file data to be mapped in the mapped view.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



At least <i>numElements</i> bytes must be available in the mapped view, but depending on the application, more bytes may actually be mapped. The data must be 8-byte aligned relative to the file offset. For example, the data at file offset 0x8001 must be mapped to some memory location whose address modulo 8 is 1.




## -see-also




<a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a>
 

 

