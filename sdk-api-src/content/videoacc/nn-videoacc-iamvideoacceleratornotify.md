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

# IAMVideoAcceleratorNotify interface


## -description


The <b>IAMVideoAcceleratorNotify</b> interface is a callback interface used in conjunction with the <a href="https://msdn.microsoft.com/78e0a165-5a19-4dca-8d6c-445345772824">IAMVideoAccelerator</a> interface. It enables the video renderer filter to communicate with the video decoder when configuring 
        
      DirectX Video Acceleration (DXVA) decoding.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoAcceleratorNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVideoAcceleratorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoAcceleratorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72e3331d-1e54-4ec7-9972-7e39eaf2707d">GetCreateVideoAcceleratorData</a>
</td>
<td align="left" width="63%">
Gets information needed to create a video accelerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee8cbe71-6ac3-4f41-a9af-f372f825485d">GetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e82c73e6-d32e-4875-9f9d-124a1c6ce504">SetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Notifies the decoder of how many uncompressed surfaces were created.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fd72be3-4ff5-4c93-8055-abe247f3c856">DirectShow Reference</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>
 

 

