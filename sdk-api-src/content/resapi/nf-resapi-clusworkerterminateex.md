---
UID: NF:resapi.ClusWorkerTerminateEx
title: ClusWorkerTerminateEx function (resapi.h)
description: Waits for a worker thread to terminate up to the specified timeout. (ClusWorkerTerminateEx)
helpviewer_keywords: ["ClusWorkerTerminateEx","ClusWorkerTerminateEx function [Failover Cluster]","mscs.clusworkerterminateex","resapi/ClusWorkerTerminateEx"]
old-location: mscs\clusworkerterminateex.htm
tech.root: MsCS
ms.assetid: e2dda7c0-01d4-49e5-bc57-3fa07495d536
ms.date: 12/05/2018
ms.keywords: ClusWorkerTerminateEx, ClusWorkerTerminateEx function [Failover Cluster], mscs.clusworkerterminateex, resapi/ClusWorkerTerminateEx
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
 - ClusWorkerTerminateEx
 - resapi/ClusWorkerTerminateEx
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
 - ClusWorkerTerminateEx
---

# ClusWorkerTerminateEx function


## -description

Waits for a worker thread to terminate up to the specified timeout.  This function can signal the thread to terminate before wait starts, or just wait passively if specified.

## -parameters

### -param ClusWorker [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure describing the 
       worker thread to terminate.

### -param TimeoutInMilliseconds [in]

The timeout in milliseconds.

### -param WaitOnly [in]

If set <b>TRUE</b>, the function will wait for up to specified timeout without signaling the thread to terminate; otherwise it will signal the thread to terminate before waiting for the thread.

## -returns

Returns a system error code on failure.

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
The worker thread is not terminated within the specified timeout.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercheckterminate">ClusWorkerCheckTerminate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkerterminate">ClusWorkerTerminate</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkersterminate">ClusWorkersTerminate</a>



<a href="/previous-versions/windows/desktop/mscs/thread-management-utility-functions">Thread Management Utility Functions</a>
