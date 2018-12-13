---
UID: NN:audioengineendpoint.IAudioInputEndpointRT
title: IAudioInputEndpointRT
author: windows-sdk-content
description: Gets the input buffer for each processing pass.
old-location: termserv\iaudioinputendpointrt.htm
tech.root: TermServ
ms.assetid: f9638dea-f61d-45f6-b91d-72e4fc1b4a92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioInputEndpointRT, IAudioInputEndpointRT interface [Remote Desktop Services], IAudioInputEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioInputEndpointRT, termserv.iaudioinputendpointrt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioInputEndpointRT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioInputEndpointRT interface


## -description


Gets the input buffer for each processing pass.The 
    <b>IAudioInputEndpointRT</b> interface is used by the 
    audio engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioInputEndpointRT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioInputEndpointRT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioInputEndpointRT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1da81a49-d421-4643-9be6-b13d45d678f0">GetInputDataPointer</a>
</td>
<td align="left" width="63%">
Gets a pointer to the buffer from which data will be read by the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b23eac3-48e2-4d58-be6c-878967e7fa5c">PulseEndpoint</a>
</td>
<td align="left" width="63%">
This method is  reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dd3f72a-79fe-4d07-a301-d0960e30a2d1">ReleaseInputDataPointer</a>
</td>
<td align="left" width="63%">
Releases the acquired data pointer.

</td>
</tr>
</table> 


## -remarks



<b>IAudioInputEndpointRT</b> methods can be called 
     from a real-time processing thread. The implementation of the methods of this interface must not block, access 
     paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



