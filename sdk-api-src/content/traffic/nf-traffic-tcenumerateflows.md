---
UID: NF:traffic.TcEnumerateFlows
title: TcEnumerateFlows function (traffic.h)
description: The TcEnumerateFlows function enumerates installed flows and their associated filters on an interface.
helpviewer_keywords: ["TcEnumerateFlows","TcEnumerateFlows function [QOS]","_gqos_tcenumerateflows","qos.tcenumerateflows","traffic/TcEnumerateFlows"]
old-location: qos\tcenumerateflows.htm
tech.root: QOS
ms.assetid: eae90fae-a29a-4005-b8c6-a5e2c9a6c07f
ms.date: 12/05/2018
ms.keywords: TcEnumerateFlows, TcEnumerateFlows function [QOS], _gqos_tcenumerateflows, qos.tcenumerateflows, traffic/TcEnumerateFlows
req.header: traffic.h
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
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TcEnumerateFlows
 - traffic/TcEnumerateFlows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcEnumerateFlows
---

# TcEnumerateFlows function


## -description

The 
<b>TcEnumerateFlows</b> function enumerates installed flows and their associated filters on an interface.

The process of returning flow enumeration often consists of multiple calls to the 
<b>TcEnumerateFlows</b> function. The process of receiving flow information from 
<b>TcEnumerateFlows</b> can be compared to reading through a book in multiple sittings, where a certain number of pages are read at one time, a bookmark is placed where reading stops, reading is resumed at the bookmark, and continues until the book is finished.

The 
<b>TcEnumerateFlows</b> function fills the <i>Buffer</i> parameter with as many flow enumerations as the buffer can hold, then returns a handle in the pEnumToken parameter that internally bookmarks where the enumeration stopped. Subsequent calls to 
<b>TcEnumerateFlows</b> must then pass the returned <i>pEnumToken</i> value to instruct traffic control where to resume flow enumeration information. When all flows have been enumerated, <i>pEnumToken</i> will be <b>NULL</b>.

## -parameters

### -param IfcHandle [in]

Handle associated with the interface on which flows are to be enumerated. This handle is obtained by a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a> function.

### -param pEnumHandle [in, out]

Pointer to the enumeration token, used internally by traffic control to maintain returned flow information state. 




For input of the initial call to 
<b>TcEnumerateFlows</b>, <i>pEnumToken</i> should be set to <b>NULL</b>. For input on subsequent calls, <i>pEnumToken</i> must be the value returned as the <i>pEnumToken</i> OUT parameter from the immediately preceding call to 
<b>TcEnumerateFlows</b>.

For output, <i>pEnumToken</i> is the refreshed enumeration token that must be used in the following call to 
<b>TcEnumerateFlows</b>.

### -param pFlowCount [in, out]

Pointer to the number of requested or returned flows. For input, this parameter designates the number of requested flows or it can be set to <b>0xFFFF</b> to request all flows. For output, <i>pFlowCount</i> returns the number of flows actually returned in <i>Buffer</i>.

### -param pBufSize [in, out]

Pointer to the size of the client-provided buffer or the number of bytes used by traffic control. For input, points to the size of <i>Buffer</i>, in bytes. For output, points to the actual amount of buffer space, in bytes, written or needed with flow enumerations.

### -param Buffer [out]

Pointer to the buffer containing flow enumerations. See 
<a href="/windows/desktop/api/traffic/ns-traffic-enumeration_buffer">ENUMERATION_BUFFER</a> for more information about flow enumerations.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the pointers is <b>NULL</b>, or <i>pFlowCount</i> or <i>pBufSize</i> are set to zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to store even a single flow's information and attached filters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The enumeration token is no longer valid.

</td>
</tr>
</table>

## -remarks

Do not request zero flows, or pass a buffer with a size equal to zero or pointer to a <b>NULL</b>.

If an enumeration token pointer has been invalidated by traffic control (due to the deletion of a flow), continuing to enumerate flows is not allowed, and the call will return ERROR_INVALID_DATA. Under this circumstance, the process of enumeration must start over. This circumstance can occur when the next flow to be enumerated is deleted while enumeration is in progress.

To get the total number of flows for a given interface, call 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcqueryinterface">TcQueryInterface</a> and specify <b>GUID_QOS_FLOW_COUNT</b>.

<div class="alert"><b>Note</b>  Use of the 
<b>TcEnumerateFlows</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcqueryinterface">TcQueryInterface</a>