---
UID: NN:strmif.IMediaSample2
title: IMediaSample2
author: windows-sdk-content
description: The IMediaSample2 interface sets and retrieves properties on media samples.This interface inherits the IMediaSample interface.
old-location: dshow\imediasample2.htm
tech.root: DirectShow
ms.assetid: 638cb75d-9be6-4ba1-a116-47e2d62b689d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IMediaSample2, IMediaSample2 interface [DirectShow], IMediaSample2 interface [DirectShow],described, IMediaSample2Interface, dshow.imediasample2, strmif/IMediaSample2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
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
 - IMediaSample2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample2 interface


## -description



The <code>IMediaSample2</code> interface sets and retrieves properties on media samples.

This interface inherits the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface. Whereas the <b>IMediaSample</b> interface requires separate method calls for each sample property, the <code>IMediaSample2</code> interface has methods for setting and retrieving multiple properties at once.

Media samples are not guaranteed to support <code>IMediaSample2</code>. However, if an allocator creates samples that support <code>IMediaSample2</code>, all of the samples that it creates must support the interface. For any given media sample, the <b>IMediaSample2::GetProperties</b> method returns the same values as the individual <b>IMediaSample</b> methods. Therefore, you can use whichever version you prefer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSample2</b> interface inherits from <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a>. <b>IMediaSample2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaSample2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef20deed-f906-459a-8c2a-f1c929ade9ac">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of a media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f024fe3a-802d-4dc1-9f4d-ebeeed0b067a">SetProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of a media sample.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a>
 

 

