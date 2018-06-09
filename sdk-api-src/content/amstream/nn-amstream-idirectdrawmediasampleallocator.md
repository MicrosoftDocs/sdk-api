---
UID: NN:amstream.IDirectDrawMediaSampleAllocator
title: IDirectDrawMediaSampleAllocator
author: windows-sdk-content
description: The IDirectDrawMediaSampleAllocator interface allocates samples that contain DirectDraw surfaces.The Overlay Mixer filter's input pin creates an allocator that implements this interface.
old-location: dshow\idirectdrawmediasampleallocator.htm
old-project: DirectShow
ms.assetid: 35fd81ce-058a-4caf-b1de-f669be586f33
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IDirectDrawMediaSampleAllocator, IDirectDrawMediaSampleAllocator interface [DirectShow], IDirectDrawMediaSampleAllocator interface [DirectShow],described, IDirectDrawMediaSampleAllocatorInterface, amstream/IDirectDrawMediaSampleAllocator, dshow.idirectdrawmediasampleallocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: amstream.h
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
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawMediaSampleAllocator
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawMediaSampleAllocator interface


## -description



The <code>IDirectDrawMediaSampleAllocator</code> interface allocates samples that contain DirectDraw surfaces.

The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter's input pin creates an allocator that implements this interface. This allocator allocates <a href="https://msdn.microsoft.com/0a83b257-e88f-4870-924c-56ddc325f17f">IDirectDrawMediaSample</a> media samples that also support the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface.

Decoder filters should not have to use this interface to connect to the Overlay Mixer. Applications never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawMediaSampleAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawMediaSampleAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawMediaSampleAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6eed9d-635d-424b-ba14-213bbe56f66c">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw instance used to allocate surfaces.

</td>
</tr>
</table> 

