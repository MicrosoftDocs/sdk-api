---
UID: NN:vfw.IAVIStreaming
title: IAVIStreaming (vfw.h)
author: windows-sdk-content
description: The IAVIStreaming interface supports preparing open data streams for playback in streaming operations. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
The IAVIStreaming interface supports preparing open data streams for playback in streaming operations. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavistreaming.htm
tech.root: Multimedia
ms.assetid: ff8ed190-5e90-4be1-8f14-0d288ce0837c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAVIStreaming, IAVIStreaming interface [Windows Multimedia], IAVIStreaming interface [Windows Multimedia],described, _win32_IAVIStreaming, multimedia.iavistreaming, vfw/IAVIStreaming
ms.topic: interface
f1_keywords: 
 - "vfw/IAVIStreaming"
req.header: vfw.h
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStreaming
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAVIStreaming interface


## -description



The <b>IAVIStreaming</b> interface supports preparing open data streams for playback in streaming operations. Uses <a href="https://docs.microsoft.com/previous-versions/dd757101(v=vs.85)">IUnknown::QueryInterface</a>, <a href="https://docs.microsoft.com/previous-versions/dd757100(v=vs.85)">IUnknown::AddRef</a>, <a href="https://docs.microsoft.com/previous-versions/dd757102(v=vs.85)">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIStreaming</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAVIStreaming</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIStreaming</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistreaming-begin">Begin</a>
</td>
<td align="left" width="63%">
Prepares for the streaming operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iavistreaming-end">End</a>
</td>
<td align="left" width="63%">
Ends the streaming operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>
 

 

