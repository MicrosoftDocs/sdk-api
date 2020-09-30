---
UID: NN:audioengineendpoint.IAudioInputEndpointRT
title: IAudioInputEndpointRT (audioengineendpoint.h)
description: Gets the input buffer for each processing pass.
helpviewer_keywords: ["IAudioInputEndpointRT","IAudioInputEndpointRT interface [Remote Desktop Services]","IAudioInputEndpointRT interface [Remote Desktop Services]","described","audioengineendpoint/IAudioInputEndpointRT","termserv.iaudioinputendpointrt"]
old-location: termserv\iaudioinputendpointrt.htm
tech.root: TermServ
ms.assetid: f9638dea-f61d-45f6-b91d-72e4fc1b4a92
ms.date: 12/05/2018
ms.keywords: IAudioInputEndpointRT, IAudioInputEndpointRT interface [Remote Desktop Services], IAudioInputEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioInputEndpointRT, termserv.iaudioinputendpointrt
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioInputEndpointRT
 - audioengineendpoint/IAudioInputEndpointRT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioInputEndpointRT
---

# IAudioInputEndpointRT interface


## -description

Gets the input buffer for each processing pass.The 
    <b>IAudioInputEndpointRT</b> interface is used by the 
    audio engine.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioInputEndpointRT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioInputEndpointRT</b> also has these types of members:
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
<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">GetInputDataPointer</a>
</td>
<td align="left" width="63%">
Gets a pointer to the buffer from which data will be read by the audio engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-pulseendpoint">PulseEndpoint</a>
</td>
<td align="left" width="63%">
This method is  reserved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-releaseinputdatapointer">ReleaseInputDataPointer</a>
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