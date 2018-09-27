---
UID: NF:resapi.ResUtilTerminateServiceProcessFromResDll
title: ResUtilTerminateServiceProcessFromResDll function
author: windows-sdk-content
description: Attempts to terminate the process of a service being managed as a cluster resource by a resource DLL. The PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL type defines a pointer to this function.
old-location: mscs\resutilterminateserviceprocessfromresdll.htm
tech.root: mscs
ms.assetid: 8ac3bd90-a717-479c-b976-9ef536853ffe
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL, PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL function [Failover Cluster], ResUtilTerminateServiceProcessFromResDll, ResUtilTerminateServiceProcessFromResDll function [Failover Cluster], _wolf_resutilterminateserviceprocessfromresdll, mscs.resutilterminateserviceprocessfromresdll, resapi/PRESUTIL_TERMINATE_SERVICE_PROCESS_FROM_RES_DLL, resapi/ResUtilTerminateServiceProcessFromResDll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilTerminateServiceProcessFromResDll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
       <a href="https://msdn.microsoft.com/c3897c96-743e-4753-8fef-b8defe4f2b00">GetClusterResourceState</a>). Pass 
       <b>NULL</b> if you don't need this information.


### -param pfnLogEvent [in]

Pointer to the <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> function used by your resource 
       DLL. This pointer is passed to your resource DLL in the 
       <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a> entry point.


### -param hResourceHandle [in]

The Resource Monitor's handle to the resource. This handle is passed to your resource DLL in the 
       <a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a> entry point and must be saved as part of the resource's 
       <a href="https://msdn.microsoft.com/0580ec99-2bb7-440b-9a5b-a73430b5b0f1">instance data</a>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the 
       operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.

Note that 
       <b>ResUtilTerminateServiceProcessFromResDll</b> 
       uses <i>pfnLogEvent</i> and <i>hResourceHandle</i> to write to your 
       resource DLL's event log, which may help troubleshoot failures.




## -remarks



You should only call 
    <b>ResUtilTerminateServiceProcessFromResDll</b> 
    when terminating a resource or when taking a resource offline.




## -see-also




<a href="https://msdn.microsoft.com/16fcc65f-81b3-4126-a56e-4aaee3099b8c">Service Utility Functions</a>
 

 

