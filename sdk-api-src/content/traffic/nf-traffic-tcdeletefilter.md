---
UID: NF:traffic.TcDeleteFilter
title: TcDeleteFilter function (traffic.h)
description: The TcDeleteFilter function deletes a filter previously added with the TcAddFilter function.
helpviewer_keywords: ["TcDeleteFilter","TcDeleteFilter function [QOS]","_gqos_tcdeletefilter","qos.tcdeletefilter","traffic/TcDeleteFilter"]
old-location: qos\tcdeletefilter.htm
tech.root: QOS
ms.assetid: 3a9eaffc-78d8-4473-a2d3-c060b104abd3
ms.date: 12/05/2018
ms.keywords: TcDeleteFilter, TcDeleteFilter function [QOS], _gqos_tcdeletefilter, qos.tcdeletefilter, traffic/TcDeleteFilter
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
 - TcDeleteFilter
 - traffic/TcDeleteFilter
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
 - TcDeleteFilter
---

# TcDeleteFilter function


## -description

The 
<b>TcDeleteFilter</b> function deletes a filter previously added with the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddfilter">TcAddFilter</a> function.

## -parameters

### -param FilterHandle [in]

Handle to the filter to be deleted, as received in a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddfilter">TcAddFilter</a> function.

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
The filter handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Use of the 
<b>TcDeleteFilter</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddfilter">TcAddFilter</a>