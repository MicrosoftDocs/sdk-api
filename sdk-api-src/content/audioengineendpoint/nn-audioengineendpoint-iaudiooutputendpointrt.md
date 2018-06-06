---
UID: NN:audioengineendpoint.IAudioOutputEndpointRT
title: IAudioOutputEndpointRT
author: windows-sdk-content
description: Gets the output buffer for each processing pass.
old-location: termserv\iaudiooutputendpointrt.htm
old-project: TermServ
ms.assetid: b881b2f9-ffe9-46ff-94aa-eef0af172a3e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IAudioOutputEndpointRT, IAudioOutputEndpointRT interface [Remote Desktop Services], IAudioOutputEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioOutputEndpointRT, termserv.iaudiooutputendpointrt
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioOutputEndpointRT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioOutputEndpointRT interface


## -description


Gets the output buffer for each processing pass. The  
    <b>IAudioOutputEndpointRT</b> interface is used by the 
    audio engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioOutputEndpointRT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioOutputEndpointRT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioOutputEndpointRT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14d69520-3d0c-42ee-8986-9d83b5cff62e">GetOutputDataPointer</a>
</td>
<td align="left" width="63%">
Gets a pointer to the output buffer in which data will be written by the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ab117d6-5b13-4420-9cf2-865ff2011806">PulseEndpoint</a>
</td>
<td align="left" width="63%">
This method is  reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55b7d55e-b684-4c6e-a937-e8922732857d">ReleaseOutputDataPointer</a>
</td>
<td align="left" width="63%">
Releases the pointer to the output buffer.

</td>
</tr>
</table> 


## -remarks



<b>IAudioOutputEndpointRT</b> methods can be called 
     from a real-time processing thread. The implementation of the methods of this interface must not block, access 
     paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



