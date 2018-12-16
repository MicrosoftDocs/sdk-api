---
UID: NN:amstream.IDirectDrawMediaSampleAllocator
title: IDirectDrawMediaSampleAllocator
author: windows-sdk-content
description: The IDirectDrawMediaSampleAllocator interface allocates samples that contain DirectDraw surfaces.The Overlay Mixer filter's input pin creates an allocator that implements this interface.
old-location: dshow\idirectdrawmediasampleallocator.htm
tech.root: DirectShow
ms.assetid: 35fd81ce-058a-4caf-b1de-f669be586f33
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDrawMediaSampleAllocator, IDirectDrawMediaSampleAllocator interface [DirectShow], IDirectDrawMediaSampleAllocator interface [DirectShow],described, IDirectDrawMediaSampleAllocatorInterface, amstream/IDirectDrawMediaSampleAllocator, dshow.idirectdrawmediasampleallocator
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
 - IDirectDrawMediaSampleAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawMediaSampleAllocator interface


## -description



The <code>IDirectDrawMediaSampleAllocator</code> interface allocates samples that contain DirectDraw surfaces.

The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter's input pin creates an allocator that implements this interface. This allocator allocates <a href="https://msdn.microsoft.com/en-us/library/Dd406801(v=VS.85).aspx">IDirectDrawMediaSample</a> media samples that also support the <a href="https://msdn.microsoft.com/en-us/library/Dd407001(v=VS.85).aspx">IMediaSample</a> interface.

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
<a href="https://msdn.microsoft.com/en-us/library/Dd406803(v=VS.85).aspx">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw instance used to allocate surfaces.

</td>
</tr>
</table> 

