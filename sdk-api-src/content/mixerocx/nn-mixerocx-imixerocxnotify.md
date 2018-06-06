---
UID: NN:mixerocx.IMixerOCXNotify
title: IMixerOCXNotify
author: windows-sdk-content
description: The IMixerOCXNotify interface is implemented by clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.
old-location: dshow\imixerocxnotify.htm
old-project: DirectShow
ms.assetid: b73416c0-2312-4164-8a6d-f8776dc1447f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMixerOCXNotify, IMixerOCXNotify interface [DirectShow], IMixerOCXNotify interface [DirectShow],described, IMixerOCXNotifyInterface, dshow.imixerocxnotify, mixerocx/IMixerOCXNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mixerocx.h
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
tech.root: 
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerOCXNotify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerOCXNotify interface


## -description



The <code>IMixerOCXNotify</code> interface is implemented by clients and called by the Overlay Mixer to send notifications of events affecting the video display rectangle.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMixerOCXNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMixerOCXNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMixerOCXNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8080e5f-99e7-47eb-96ff-53c4ed8d2ff1">OnDataChange</a>
</td>
<td align="left" width="63%">
Notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55d349d4-1a9a-4762-8058-c3f7a559e272">OnInvalidateRect</a>
</td>
<td align="left" width="63%">
Notifies the client that the video rectangle has been invalidated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6e49306-59bc-45a2-826b-cea2cf77214b">OnStatusChange</a>
</td>
<td align="left" width="63%">
Notifies the client that a status change has occurred.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>
 

 

