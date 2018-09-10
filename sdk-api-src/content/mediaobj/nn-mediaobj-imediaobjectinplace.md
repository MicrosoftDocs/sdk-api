---
UID: NN:mediaobj.IMediaObjectInPlace
title: IMediaObjectInPlace
author: windows-sdk-content
description: The IMediaObjectInPlace interface provides methods for processing data in place. A Microsoft DirectX Media Object (DMO) can expose this interface if it meets the following conditions:\_
The IMediaObjectInPlace interface provides methods for processing data in place. A Microsoft DirectX Media Object (DMO) can expose this interface if it meets the following conditions:This interface provides an optimized way to process data. The application calls a single IMediaObjectInPlace::Process method instead of the IMediaObject::ProcessInput and IMediaObject::ProcessOutput methods. However, any DMO that implements this interface must also implement the IMediaObject interface. Therefore, an application is never obligated to use this interface, and a DMO is never guaranteed to implement it.
old-location: dshow\imediaobjectinplace.htm
tech.root: DirectShow
ms.assetid: c2105141-6c5e-4edb-aa3b-3227ca223329
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IMediaObjectInPlace, IMediaObjectInPlace interface [DirectShow], IMediaObjectInPlace interface [DirectShow],described, IMediaObjectInPlaceInterface, dshow.imediaobjectinplace, mediaobj/IMediaObjectInPlace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObjectInPlace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObjectInPlace interface


## -description



The <code>IMediaObjectInPlace</code> interface provides methods for processing data in place. A Microsoft DirectX Media Object (DMO) can expose this interface if it meets the following conditions:


<ul>
<li>It has one input stream and one output stream.</li>
<li>Both streams use the same media type.</li>
<li>The output is produced in place on the buffer; that is, without copying data.</li>
</ul>This interface provides an optimized way to process data. The application calls a single <a href="https://msdn.microsoft.com/567117cd-db7b-4764-9c88-ab898a64b56a">IMediaObjectInPlace::Process</a> method instead of the <a href="https://msdn.microsoft.com/f52e9586-f65d-418f-8c1a-c97c0a81d253">IMediaObject::ProcessInput</a> and <a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a> methods. However, any DMO that implements this interface must also implement the <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> interface. Therefore, an application is never obligated to use this interface, and a DMO is never guaranteed to implement it.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaObjectInPlace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaObjectInPlace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaObjectInPlace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6660afa8-3502-4e88-925b-192e06346243">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the DMO in its current state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6ed4824-bc18-4a12-82d3-d68e98f6d964">GetLatency</a>
</td>
<td align="left" width="63%">
Retrieves the latency introduced by this DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/567117cd-db7b-4764-9c88-ab898a64b56a">Process</a>
</td>
<td align="left" width="63%">
Processes a block of data.

</td>
</tr>
</table> 

