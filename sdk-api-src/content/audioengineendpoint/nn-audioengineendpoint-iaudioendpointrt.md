---
UID: NN:audioengineendpoint.IAudioEndpointRT
title: IAudioEndpointRT (audioengineendpoint.h)
author: windows-sdk-content
description: Gets the difference between the current read and write positions in the endpoint buffer.
old-location: termserv\iaudioendpointrt.htm
tech.root: TermServ
ms.assetid: 3fb05ce4-a3be-4c84-8e03-71213f453f74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointRT, IAudioEndpointRT interface [Remote Desktop Services], IAudioEndpointRT interface [Remote Desktop Services],described, audioengineendpoint/IAudioEndpointRT, termserv.iaudioendpointrt
ms.topic: interface
f1_keywords: 
 - "audioengineendpoint/IAudioEndpointRT"
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
 - IAudioEndpointRT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointRT interface


## -description


Gets the difference between the current read and write positions in the endpoint buffer. The 
    <b>IAudioEndpointRT</b> interface is used by the audio 
    engine.

<b>IAudioEndpointRT</b> methods can be called from a 
    real-time processing thread. The implementation of the methods of this interface must not block, access paged 
    memory, or call any blocking system routines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointRT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointRT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointRT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointrt-getcurrentpadding">GetCurrentPadding</a>
</td>
<td align="left" width="63%">
Gets the amount, in 100-nanosecond units, of data that is queued up in the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointrt-processingcomplete">ProcessingComplete</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that a processing pass has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointrt-setpinactive">SetPinActive</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that it must change the state of the underlying stream to an active state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointrt-setpininactive">SetPinInactive</a>
</td>
<td align="left" width="63%">
Notifies the endpoint that it must change the state of the underlying stream to an inactive state.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



