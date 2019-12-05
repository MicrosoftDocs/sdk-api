---
UID: NN:audioengineendpoint.IAudioEndpointControl
title: IAudioEndpointControl (audioengineendpoint.h)
description: Controls the stream state of an endpoint.
old-location: termserv\iaudioendpointcontrol.htm
tech.root: TermServ
ms.assetid: 4514521a-e9a9-4f39-ab7d-4ef7e514bd10
ms.date: 12/05/2018
ms.keywords: IAudioEndpointControl, IAudioEndpointControl interface [Remote Desktop Services], IAudioEndpointControl interface [Remote Desktop Services],described, audioengineendpoint/IAudioEndpointControl, termserv.iaudioendpointcontrol
ms.topic: interface
f1_keywords:
- audioengineendpoint/IAudioEndpointControl
dev_langs:
- c++
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
- IAudioEndpointControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointControl interface


## -description


Controls the stream state of an endpoint.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointcontrol-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the endpoint stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointcontrol-start">Start</a>
</td>
<td align="left" width="63%">
Starts the endpoint stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointcontrol-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the endpoint stream.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.



