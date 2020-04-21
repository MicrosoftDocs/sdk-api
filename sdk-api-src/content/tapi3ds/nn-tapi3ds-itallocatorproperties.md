---
UID: NN:tapi3ds.ITAllocatorProperties
title: ITAllocatorProperties (tapi3ds.h)
description: The ITAllocatorProperties interface exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application.helpviewer_keywords: ["ITAllocatorProperties","ITAllocatorProperties interface [TAPI 2.2]","ITAllocatorProperties interface [TAPI 2.2]","described","_tapi3_itallocatorproperties","tapi3.itallocatorproperties","tapi3ds/ITAllocatorProperties"]
old-location: tapi3\itallocatorproperties.htm
tech.root: Tapi
ms.assetid: a0facf08-1b03-415b-b97e-3fda5a164b89
ms.date: 12/05/2018
ms.keywords: ITAllocatorProperties, ITAllocatorProperties interface [TAPI 2.2], ITAllocatorProperties interface [TAPI 2.2],described, _tapi3_itallocatorproperties, tapi3.itallocatorproperties, tapi3ds/ITAllocatorProperties
f1_keywords:
- tapi3ds/ITAllocatorProperties
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAllocatorProperties interface


## -description


The 
<b>ITAllocatorProperties</b> interface exposes the buffer allocator properties of the Media Streaming Terminal (MST) to an end-user or server application. An application needs to tune the sample size for a particular protocol. The decision concerning appropriate properties is highly implementation dependent.

This interface is exposed on the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a> by the associated Media Service Provider. If it exists, a <b>QueryInterface</b> on any Terminal interface, such as 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>, can be used to obtain an 
<b>ITAllocatorProperties</b> pointer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAllocatorProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITAllocatorProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-getallocatebuffers">GetAllocateBuffers</a>
</td>
<td align="left" width="63%">
Gets whether buffers must be supplied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-getallocatorproperties">GetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Gets the negotiated allocator properties following a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-getbuffersize">GetBufferSize</a>
</td>
<td align="left" width="63%">
Gets the size of the allocator buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-setallocatebuffers">SetAllocateBuffers</a>
</td>
<td align="left" width="63%">
Sets whether buffers must be supplied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-setallocatorproperties">SetAllocatorProperties</a>
</td>
<td align="left" width="63%">
Forces MST to use the values input during filter negotiation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itallocatorproperties-setbuffersize">SetBufferSize</a>
</td>
<td align="left" width="63%">
Sets the size of the allocator buffer.

</td>
</tr>
</table> 

