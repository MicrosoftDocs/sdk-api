---
UID: NN:amstream.IDirectDrawMediaSampleAllocator
title: IDirectDrawMediaSampleAllocator (amstream.h)
author: windows-sdk-content
description: The IDirectDrawMediaSampleAllocator interface allocates samples that contain DirectDraw surfaces.The Overlay Mixer filter's input pin creates an allocator that implements this interface.
old-location: dshow\idirectdrawmediasampleallocator.htm
tech.root: DirectShow
ms.assetid: 35fd81ce-058a-4caf-b1de-f669be586f33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaSampleAllocator, IDirectDrawMediaSampleAllocator interface [DirectShow], IDirectDrawMediaSampleAllocator interface [DirectShow],described, IDirectDrawMediaSampleAllocatorInterface, amstream/IDirectDrawMediaSampleAllocator, dshow.idirectdrawmediasampleallocator
ms.topic: interface
f1_keywords: 
 - "amstream/IDirectDrawMediaSampleAllocator"
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
ms.custom: 19H1
---

# IDirectDrawMediaSampleAllocator interface


## -description



The <code>IDirectDrawMediaSampleAllocator</code> interface allocates samples that contain DirectDraw surfaces.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter's input pin creates an allocator that implements this interface. This allocator allocates <a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample">IDirectDrawMediaSample</a> media samples that also support the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample</a> interface.

Decoder filters should not have to use this interface to connect to the Overlay Mixer. Applications never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawMediaSampleAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawMediaSampleAllocator</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-idirectdrawmediasampleallocator-getdirectdraw">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw instance used to allocate surfaces.

</td>
</tr>
</table> 

