---
UID: NN:bdaiface.IEnumPIDMap
title: IEnumPIDMap
author: windows-sdk-content
description: The IEnumPIDMap interface enumerates a collection of Packet ID (PID) maps.
old-location: dshow\ienumpidmap.htm
tech.root: DirectShow
ms.assetid: d46010c4-0f16-4c97-ad10-16f7ac250390
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IEnumPIDMap, IEnumPIDMap interface [DirectShow], IEnumPIDMap interface [DirectShow],described, IEnumPIDMapInterface, bdaiface/IEnumPIDMap, dshow.ienumpidmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
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
 - IEnumPIDMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPIDMap interface


## -description



The <code>IEnumPIDMap</code> interface enumerates a collection of Packet ID (PID) maps. Each PID map describes how the <a href="https://msdn.microsoft.com/99bfc55d-6519-4e85-98ce-cad27bd71ffb">MPEG-2 Demultiplexer</a> filter maps a PID to an output pin on the filter. PID mappings are created by calling the <a href="https://msdn.microsoft.com/22784e4a-2b02-4fc9-ba55-8c918ea38892">IMPEG2PIDMap::MapPID</a> method on the filter's output pin.

To obtain the <code>IEnumPIDMap</code> interface, call the <a href="https://msdn.microsoft.com/9e5dbc92-e072-4e59-b7b2-07ae39cb9d59">IMPEG2PIDMap::EnumPIDMap</a> method on the output pin. Typically, output pins for audio and video streams have at most one PID mapped at any given time.

This interface implements a standard Component Object Model (COM) collection object. The collection object represents a snapshot of the PID map when the collection is created. The collection is not updated automatically.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPIDMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPIDMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPIDMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d965a71-ff5e-4d4a-8976-0de5b8bbae04">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7e3a2a7-cc62-478d-b0b8-30d58f0b3372">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f5cc44e-10c0-441f-b34c-80f94c5f6bca">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e611e5a0-beb1-4a31-974a-29b2b8349a17">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of elements in the collection.

</td>
</tr>
</table> 

