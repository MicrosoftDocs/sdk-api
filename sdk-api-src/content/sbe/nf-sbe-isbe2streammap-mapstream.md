---
UID: NF:sbe.ISBE2StreamMap.MapStream
title: ISBE2StreamMap::MapStream
author: windows-sdk-content
description: Maps a stream to an output pin for a Stream Buffer Source filter.
old-location: mstv\isbe2streammap_mapstream.htm
old-project: mstv
ms.assetid: efe3b21d-9664-4367-9bfe-4c02589370c4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISBE2StreamMap interface [Microsoft TV Technologies],MapStream method, ISBE2StreamMap.MapStream, ISBE2StreamMap::MapStream, MapStream, MapStream method [Microsoft TV Technologies], MapStream method [Microsoft TV Technologies],ISBE2StreamMap interface, mstv.isbe2streammap_mapstream, sbe/ISBE2StreamMap::MapStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2StreamMap.MapStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISBE2StreamMap::MapStream


## -description


Maps a stream to an output pin for a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter.

By default, the stream mappings cannot be changed. Before calling this method, disable the default mapping mode by calling the <a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">ISBE2Crossbar::EnableDefaultMode</a> method without the <b>DEF_MODE_STREAMS</b> flag.


## -parameters




### -param Stream [in]

Identifier for the stream mapped to an output pin. The major type of the stream must match the major type of the pin.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified stream has already been mapped to a pin.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot unmap the stream, because the default mode is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_NOT_FOUND)</b></dt>
<dt>0x80070490</dt>
</dl>
</td>
<td width="60%">
No stream exists with the specified stream identifier.

</td>
</tr>
</table>
 




## -remarks



If the new stream has different media type from the previously mapped stream, the output pin follows the dynamic format change procedure described in <a href="https://msdn.microsoft.com/ff60de5a-3edc-405d-aa02-8704b96d5e87">Dynamic Format Changes</a>, and flushes downstream pins as described in <a href="https://msdn.microsoft.com/868218c4-3e1a-4da0-89fa-30a9848da0e8">Flushing</a>.




## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">ISBE2Crossbar::EnableDefaultMode</a>



<a href="https://msdn.microsoft.com/d63691ca-2420-4c54-b343-be85d634488c">ISBE2StreamMap</a>



<a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source Filter</a>
 

 

