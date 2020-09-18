---
UID: NF:traffic.TcDeregisterClient
title: TcDeregisterClient function (traffic.h)
description: The TcDeregisterClient function deregisters a client with the Traffic Control Interface (TCI).
helpviewer_keywords: ["TcDeregisterClient","TcDeregisterClient function [QOS]","_gqos_tcderegisterclient","qos.tcderegisterclient","traffic/TcDeregisterClient"]
old-location: qos\tcderegisterclient.htm
tech.root: QOS
ms.assetid: ea52b8a6-a54e-46ee-9275-734f328759ba
ms.date: 12/05/2018
ms.keywords: TcDeregisterClient, TcDeregisterClient function [QOS], _gqos_tcderegisterclient, qos.tcderegisterclient, traffic/TcDeregisterClient
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
 - TcDeregisterClient
 - traffic/TcDeregisterClient
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
 - TcDeregisterClient
---

# TcDeregisterClient function


## -description

The 
<b>TcDeregisterClient</b> function deregisters a client with the Traffic Control Interface (TCI). Before deregistering, a client must delete each installed flow and filter with the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a> and 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeletefilter">TcDeleteFilter</a> functions, and close all open interfaces with the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tccloseinterface">TcCloseInterface</a> function, respectively.

## -parameters

### -param ClientHandle [in]

Handle assigned to the client through the previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a> function.

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
Invalid interface handle, or the handle was set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TC_SUPPORTED_OBJECTS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
Interfaces are still open for this client. all interfaces must be closed to deregister a client.

</td>
</tr>
</table>

## -remarks

Once a client calls 
<b>TcDeregisterClient</b>, the only traffic control function the client is allowed to call is 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a>.

<div class="alert"><b>Note</b>  Use of the 
<b>TcDeregisterClient</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tccloseinterface">TcCloseInterface</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeletefilter">TcDeleteFilter</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a>