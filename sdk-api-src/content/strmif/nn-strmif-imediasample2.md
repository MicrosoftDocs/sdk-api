---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of a media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991815">SetProperties</a>
</td>
<td align="left" width="63%">
Sets the properties of a media sample.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a>
 

 

