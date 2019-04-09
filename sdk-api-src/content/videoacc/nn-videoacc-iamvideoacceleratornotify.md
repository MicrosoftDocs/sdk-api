---
UID: NN:videoacc.IAMVideoAcceleratorNotify
title: IAMVideoAcceleratorNotify (videoacc.h)
author: windows-sdk-content
description: The IAMVideoAcceleratorNotify interface is a callback interface used in conjunction with the IAMVideoAccelerator interface.
old-location: dshow\iamvideoacceleratornotify.htm
tech.root: DirectShow
ms.assetid: 7fd0290c-8fd6-4af6-b510-7a87bc7937de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoAcceleratorNotify, IAMVideoAcceleratorNotify interface [DirectShow], IAMVideoAcceleratorNotify interface [DirectShow],described, IAMVideoAcceleratorNotifyInterface, dshow.iamvideoacceleratornotify, videoacc/IAMVideoAcceleratorNotify
ms.topic: interface
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoAcceleratorNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoAcceleratorNotify interface


## -description


The <b>IAMVideoAcceleratorNotify</b> interface is a callback interface used in conjunction with the <a href="https://msdn.microsoft.com/en-us/library/Dd375992(v=VS.85).aspx">IAMVideoAccelerator</a> interface. It enables the video renderer filter to communicate with the video decoder when configuring 
        
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
<a href="https://msdn.microsoft.com/en-us/library/Dd375994(v=VS.85).aspx">GetCreateVideoAcceleratorData</a>
</td>
<td align="left" width="63%">
Gets information needed to create a video accelerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd375995(v=VS.85).aspx">GetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Queries the decoder for the number of uncompressed surfaces to allocate and the pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd375996(v=VS.85).aspx">SetUncompSurfacesInfo</a>
</td>
<td align="left" width="63%">
Notifies the decoder of how many uncompressed surfaces were created.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fd72be3-4ff5-4c93-8055-abe247f3c856">DirectShow Reference</a>



<a href="https://msdn.microsoft.com/0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d">How Decoders Use IAMVideoAccelerator</a>
 

 

