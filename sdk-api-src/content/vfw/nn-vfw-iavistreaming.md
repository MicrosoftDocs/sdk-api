---
UID: NN:vfw.IAVIStreaming
title: IAVIStreaming
author: windows-driver-content
description: The IAVIStreaming interface supports preparing open data streams for playback in streaming operations. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
The IAVIStreaming interface supports preparing open data streams for playback in streaming operations. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavistreaming.htm
old-project: Multimedia
ms.assetid: ff8ed190-5e90-4be1-8f14-0d288ce0837c
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IAVIStreaming, IAVIStreaming interface [Windows Multimedia], IAVIStreaming interface [Windows Multimedia], described, _win32_IAVIStreaming, multimedia.iavistreaming, vfw/IAVIStreaming
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IAVIStreaming
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# IAVIStreaming interface


## -description



The <b>IAVIStreaming</b> interface supports preparing open data streams for playback in streaming operations. Uses <a href="https://msdn.microsoft.com/6db0af58-51ee-499a-81c4-4bce8aae0f06">IUnknown::QueryInterface</a>, <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a>, <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIStreaming</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAVIStreaming</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9bd76fc3-6c31-4e29-b482-82ee0a505656">Begin</a>
</td>
<td align="left" width="63%">
Prepares for the streaming operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5db48b61-5926-41fb-9d0d-f39cba6deec9">End</a>
</td>
<td align="left" width="63%">
Ends the streaming operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

