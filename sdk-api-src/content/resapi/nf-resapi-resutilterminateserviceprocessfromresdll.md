---
UID: NF:resapi.ResUtilTerminateServiceProcessFromResDll
title: ResUtilTerminateServiceProcessFromResDll function (resapi.h)
description: Attempts to terminate the process of a service being managed as a cluster resource by a resource DLL. The PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL","PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL function [Failover Cluster]","ResUtilTerminateServiceProcessFromResDll","ResUtilTerminateServiceProcessFromResDll function [Failover Cluster]","_wolf_resutilterminateserviceprocessfromresdll","mscs.resutilterminateserviceprocessfromresdll","resapi/PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL","resapi/ResUtilTerminateServiceProcessFromResDll"]
old-location: mscs\resutilterminateserviceprocessfromresdll.htm
tech.root: MsCS
ms.assetid: 8ac3bd90-a717-479c-b976-9ef536853ffe
ms.date: 12/05/2018
ms.keywords: PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL, PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL function [Failover Cluster], ResUtilTerminateServiceProcessFromResDll, ResUtilTerminateServiceProcessFromResDll function [Failover Cluster], _wolf_resutilterminateserviceprocessfromresdll, mscs.resutilterminateserviceprocessfromresdll, resapi/PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL, resapi/ResUtilTerminateServiceProcessFromResDll
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - ResUtilTerminateServiceProcessFromResDll
 - resapi/ResUtilTerminateServiceProcessFromResDll
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
 - ResUtilTerminateServiceProcessFromResDll
---

# ResUtilTerminateServiceProcessFromResDll function


## -description

Attempts to terminate the process of a service being managed as a cluster resource by a resource DLL. The <b>PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL</b> type defines a pointer to this function.

## -parameters

### -param dwServicePid [in]

The process ID of the service process to terminate.

### -param bOffline [in]

Indicates whether the resource is being taken offline or is being terminated. Specify 
       <b>TRUE</b> if calling from the Offline entry point or from a worker thread created to take 
       the resource offline. Otherwise specify <b>FALSE</b> and the function will assume you are 
       terminating the resource.

### -param pdwResourceState [out, optional]

Optional pointer to a <b>DWORD</b> which returns the resulting state of the resource, 
       which will be either <b>ClusterResourceFailed</b> or 
       <b>ClusterResourceOffline</b> (for a complete list of resource states see 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterresourcestate">GetClusterResourceState</a>). Pass 
       <b>NULL</b> if you don't need this information.

### -param pfnLogEvent [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> function used by your resource 
       DLL. This pointer is passed to your resource DLL in the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a> entry point.

### -param hResourceHandle [in]

The Resource Monitor's handle to the resource. This handle is passed to your resource DLL in the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point and must be saved as part of the resource's 
       <a href="/previous-versions/windows/desktop/mscs/instance-data">instance data</a>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the 
       operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

Note that 
       <b>ResUtilTerminateServiceProcessFromResDll</b> 
       uses <i>pfnLogEvent</i> and <i>hResourceHandle</i> to write to your 
       resource DLL's event log, which may help troubleshoot failures.

## -remarks

You should only call 
    <b>ResUtilTerminateServiceProcessFromResDll</b> 
    when terminating a resource or when taking a resource offline.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/service-utility-functions">Service Utility Functions</a>