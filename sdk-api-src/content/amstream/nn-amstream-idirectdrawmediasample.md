---
UID: NN:amstream.IDirectDrawMediaSample
title: IDirectDrawMediaSample (amstream.h)
author: windows-sdk-content
description: The IDirectDrawMediaSample interface provides access to DirectDraw surfaces allocated by the Overlay Mixer filter.The allocator for the Overlay Mixer filter creates samples that expose this interface.
old-location: dshow\idirectdrawmediasample.htm
tech.root: DirectShow
ms.assetid: 0a83b257-e88f-4870-924c-56ddc325f17f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaSample, IDirectDrawMediaSample interface [DirectShow], IDirectDrawMediaSample interface [DirectShow],described, IDirectDrawMediaSampleInterface, amstream/IDirectDrawMediaSample, dshow.idirectdrawmediasample
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
 - IDirectDrawMediaSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawMediaSample interface


## -description



The <code>IDirectDrawMediaSample</code> interface provides access to DirectDraw surfaces allocated by the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter.

The allocator for the Overlay Mixer filter creates samples that expose this interface. These samples are used for connections between the Overlay Mixer and upstream decoder filters. Decoder filters can use this interface to unlock the DirectDraw surface while still holding it, so that other components can access the surface.

Samples that support this interface also support the <a href="https://msdn.microsoft.com/en-us/library/Dd407001(v=VS.85).aspx">IMediaSample</a> interface.

The Overlay Mixer's allocator exposes the <a href="https://msdn.microsoft.com/en-us/library/Dd406802(v=VS.85).aspx">IDirectDrawMediaSampleAllocator</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawMediaSample</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawMediaSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawMediaSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406804(v=VS.85).aspx">GetSurfaceAndReleaseLock</a>
</td>
<td align="left" width="63%">
Retrieves and unlocks the surface that the sample represents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd406805(v=VS.85).aspx">LockMediaSamplePointer</a>
</td>
<td align="left" width="63%">
Locks the surface that the sample represents.

</td>
</tr>
</table> 

