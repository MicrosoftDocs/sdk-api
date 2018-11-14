---
UID: NN:tapi3ds.ITAllocatorProperties
title: ITAllocatorProperties
author: windows-sdk-content
description: The ITAllocatorProperties interface exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application.
old-location: tapi3\itallocatorproperties.htm
tech.root: tapi
ms.assetid: a0facf08-1b03-415b-b97e-3fda5a164b89
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAllocatorProperties, ITAllocatorProperties interface [TAPI 2.2], ITAllocatorProperties interface [TAPI 2.2],described, _tapi3_itallocatorproperties, tapi3.itallocatorproperties, tapi3ds/ITAllocatorProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3ds.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAllocatorProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAllocatorProperties interface


## -description


The 
<b>ITAllocatorProperties</b> interface exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application. An application needs to tune the sample size for a particular protocol. The decision concerning appropriate properties is highly implementation dependent.

This interface is exposed on the 
<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a> by the associated Media Service Provider. If it exists, a <b>QueryInterface</b> on any Terminal interface, such as 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>, can be used to obtain an 
<b>ITAllocatorProperties</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAllocatorProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITAllocatorProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAllocatorProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74058181-ab74-4a2d-8395-c8a1a7f02820">GetAllocateBuffers</a>
</td>
<td align="left" width="63%">
Gets whether buffers must be supplied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67360904-a632-43cf-9f67-50bbdbb62f48">GetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Gets the negotiated allocator properties following a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1571bbb-345b-4b62-acb2-67afda1c9c9b">GetBufferSize</a>
</td>
<td align="left" width="63%">
Gets the size of the allocator buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4a25f8-1a5f-40ff-9a29-586d1c7c217c">SetAllocateBuffers</a>
</td>
<td align="left" width="63%">
Sets whether buffers must be supplied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ab13fac-2667-44ce-aa1a-72cd18d37b0a">SetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Forces MST to use the values input during filter negotiation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aea70fd-2078-4f51-909f-c51cb997f5ea">SetBufferSize</a>
</td>
<td align="left" width="63%">
Sets the size of the allocator buffer.

</td>
</tr>
</table> 

