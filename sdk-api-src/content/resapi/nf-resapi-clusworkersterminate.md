---
UID: NF:resapi.ClusWorkersTerminate
title: ClusWorkersTerminate function (resapi.h)
description: Waits for multiple worker threads to terminate up to the specified timeout.
helpviewer_keywords: ["ClusWorkersTerminate","ClusWorkersTerminate function [Failover Cluster]","mscs.clusworkersterminate","resapi/ClusWorkersTerminate"]
old-location: mscs\clusworkersterminate.htm
tech.root: MsCS
ms.assetid: af9bcdcf-ca92-438b-94f2-f0e7529952fb
ms.date: 12/05/2018
ms.keywords: ClusWorkersTerminate, ClusWorkersTerminate function [Failover Cluster], mscs.clusworkersterminate, resapi/ClusWorkersTerminate
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusWorkersTerminate
 - resapi/ClusWorkersTerminate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ClusWorkersTerminate
---

# ClusWorkersTerminate function


## -description



Waits for multiple  worker threads to terminate up to the specified timeout.   This function can signal the thread to terminate before wait starts, or just wait passively if specified.

## -parameters

### -param ClusWorkers [in, out]

Pointer to an array of <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structures describing the 
       threads to terminate.

### -param ClusWorkersCount [in]

The number of structures in the <i>ClusWorkers</i> parameter.

### -param TimeoutInMilliseconds [in]

The timeout in milliseconds.

### -param WaitOnly [in]

If set <b>TRUE</b>, the function will wait for up to specified timeout without signaling the thread to terminate; otherwise it will signal the thread to terminate before waiting for the thread.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
All worker threads are terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
At least one worker thread is not terminated within the specified timeout.

</td>
</tr>
</table>
 

Returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> on failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercheckterminate">ClusWorkerCheckTerminate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkerterminate">ClusWorkerTerminate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nf-resapi-clusworkerterminateex">ClusWorkerTerminateEx</a>



<a href="/previous-versions/windows/desktop/mscs/thread-management-utility-functions">Thread Management Utility Functions</a>