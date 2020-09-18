---
UID: NF:drt.DrtGetEventData
title: DrtGetEventData function (drt.h)
description: DrtGetEventData function retrieves event data associated with a signaled event.
helpviewer_keywords: ["DrtGetEventData","DrtGetEventData function [Peer Networking]","drt/DrtGetEventData","p2p.drtgeteventdata"]
old-location: p2p\drtgeteventdata.htm
tech.root: p2p
ms.assetid: 94ed3028-0bd1-449b-9902-7dbae4a70ec1
ms.date: 12/05/2018
ms.keywords: DrtGetEventData, DrtGetEventData function [Peer Networking], drt/DrtGetEventData, p2p.drtgeteventdata
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtGetEventData
 - drt/DrtGetEventData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtGetEventData
---

# DrtGetEventData function


## -description

The	<b>DrtGetEventData</b> function retrieves event data associated with a signaled event.

## -parameters

### -param hDrt [in]

Handle to the Distributed Routing Table instance for which the event occurred.

### -param ulEventDataLen [out]

The size, in bytes, of the <i>pEventData</i> buffer.

### -param pEventData [out]

Pointer to a <a href="/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a> structure that contains the event data.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT infrastructure is unaware of the requested search.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hDrt</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer is insufficient in size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
No more event data available.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_event_data">DRT_EVENT_DATA</a>