---
UID: NF:sbe.ISBE2StreamMap.UnmapStream
title: ISBE2StreamMap::UnmapStream
author: windows-sdk-content
description: Removes the mapping between a stream and an output pin for a Stream Buffer Source filter.
old-location: mstv\isbe2streammap_unmapstream.htm
tech.root: mstv
ms.assetid: 75736e65-b708-4162-836d-7694899d23d7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISBE2StreamMap interface [Microsoft TV Technologies],UnmapStream method, ISBE2StreamMap.UnmapStream, ISBE2StreamMap::UnmapStream, UnmapStream, UnmapStream method [Microsoft TV Technologies], UnmapStream method [Microsoft TV Technologies],ISBE2StreamMap interface, mstv.isbe2streammap_unmapstream, sbe/ISBE2StreamMap::UnmapStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.h
api_name:
 - ISBE2StreamMap.UnmapStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISBE2StreamMap::UnmapStream


## -description


Removes the mapping between  a stream and an output pin  for a <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter. After a successful call to this method, the output pin stops sending media samples. To resume sending media samples, the pin must be mapped to another stream by a call to the <a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">MapStream</a> method.

By default, the stream mappings cannot be changed. Before calling this method, disable the default mapping mode by calling the <a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">ISBE2Crossbar::EnableDefaultMode</a> method without the <b>DEF_MODE_STREAMS</b> flag.


## -parameters




### -param Stream [in]

Identifier for the stream. This stream will be unmapped from the output pin.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified stream does not exist or was not previously mapped to a pin.

</td>
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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Cannot unmap the stream, because the default mode is enabled.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/299816e7-2dad-44a5-a44d-9c3efe405d9b">ISBE2Crossbar</a>



<a href="https://msdn.microsoft.com/5038050b-319d-488a-9cea-a2fc59b90cc8">ISBE2Crossbar::EnableDefaultMode</a>



<a href="https://msdn.microsoft.com/d63691ca-2420-4c54-b343-be85d634488c">ISBE2StreamMap </a>



<a href="https://msdn.microsoft.com/efe3b21d-9664-4367-9bfe-4c02589370c4">ISBE2StreamMap::MapStream</a>
 

 

