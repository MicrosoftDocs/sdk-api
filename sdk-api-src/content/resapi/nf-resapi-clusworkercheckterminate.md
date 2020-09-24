---
UID: NF:resapi.ClusWorkerCheckTerminate
title: ClusWorkerCheckTerminate function (resapi.h)
description: Determines whether a worker thread should exit as soon as possible. The PCLUSAPIClusWorkerCheckTerminate type defines a pointer to this function.
helpviewer_keywords: ["ClusWorkerCheckTerminate","ClusWorkerCheckTerminate function [Failover Cluster]","PCLUSAPIClusWorkerCheckTerminate","PCLUSAPIClusWorkerCheckTerminate function [Failover Cluster]","_wolf_clusworkercheckterminate","mscs.clusworkercheckterminate","resapi/ClusWorkerCheckTerminate","resapi/PCLUSAPIClusWorkerCheckTerminate"]
old-location: mscs\clusworkercheckterminate.htm
tech.root: MsCS
ms.assetid: e8833961-ac0e-4d8c-a57e-5aabdb2c8c96
ms.date: 12/05/2018
ms.keywords: ClusWorkerCheckTerminate, ClusWorkerCheckTerminate function [Failover Cluster], PCLUSAPIClusWorkerCheckTerminate, PCLUSAPIClusWorkerCheckTerminate function [Failover Cluster], _wolf_clusworkercheckterminate, mscs.clusworkercheckterminate, resapi/ClusWorkerCheckTerminate, resapi/PCLUSAPIClusWorkerCheckTerminate
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusWorkerCheckTerminate
 - resapi/ClusWorkerCheckTerminate
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
 - ClusWorkerCheckTerminate
---

# ClusWorkerCheckTerminate function


## -description

Determines whether a worker thread should exit as soon as possible. The <b>PCLUSAPIClusWorkerCheckTerminate</b> type defines a pointer to this function.

## -parameters

### -param lpWorker [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure describing the 
       thread to check.

## -returns

<b>ClusWorkerCheckTerminate</b> returns one of 
       the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The thread should terminate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The thread should not terminate.

</td>
</tr>
</table>

## -remarks

The <b>ClusWorkerCheckTerminate</b> utility 
     function checks the <b>Terminate</b> member of the 
     <a href="/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a> structure to determine whether the thread 
     pointed to by Worker should exit. The <b>Terminate</b> member is used to prevent problems from occurring when multiple threads call 
     <a href="/windows/desktop/api/resapi/nf-resapi-clusworkerterminate">ClusWorkerTerminate</a> on the same worker thread.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clus_worker">CLUS_WORKER</a>



<a href="/windows/desktop/api/resapi/nf-resapi-clusworkercreate">ClusWorkerCreate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclusapi_clus_worker_terminate">ClusWorkerTerminate</a>



<a href="/previous-versions/windows/desktop/mscs/thread-management-utility-functions">Thread Management Utility Functions</a>