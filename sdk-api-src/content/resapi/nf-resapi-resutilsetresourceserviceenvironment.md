---
UID: NF:resapi.ResUtilSetResourceServiceEnvironment
title: ResUtilSetResourceServiceEnvironment function (resapi.h)
description: Adjusts the environment data for a service so that the service uses a cluster network name to identify its location. This function must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT","PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT function [Failover Cluster]","ResUtilSetResourceServiceEnvironment","ResUtilSetResourceServiceEnvironment function [Failover Cluster]","_wolf_resutilsetresourceserviceenvironment","mscs.resutilsetresourceserviceenvironment","resapi/PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT","resapi/ResUtilSetResourceServiceEnvironment"]
old-location: mscs\resutilsetresourceserviceenvironment.htm
tech.root: MsCS
ms.assetid: 607695f5-c542-40b8-922f-b76de6859ca7
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT, PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT function [Failover Cluster], ResUtilSetResourceServiceEnvironment, ResUtilSetResourceServiceEnvironment function [Failover Cluster], _wolf_resutilsetresourceserviceenvironment, mscs.resutilsetresourceserviceenvironment, resapi/PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT, resapi/ResUtilSetResourceServiceEnvironment
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
 - ResUtilSetResourceServiceEnvironment
 - resapi/ResUtilSetResourceServiceEnvironment
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
 - ResUtilSetResourceServiceEnvironment
---

# ResUtilSetResourceServiceEnvironment function


## -description

Adjusts the environment data for a <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a> so that the service uses a cluster network name to identify its location. This function must be called from a  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

Pointer a null-terminated Unicode string containing the name of the service.

### -param hResource [in]

Resource handle for the service obtained from  <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>.

### -param pfnLogEvent [in]

Pointer to the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function of the resource DLL managing the service.

### -param hResourceHandle [in]

Resource handle required by the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function. Use the handle passed to the DLL in the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>ResUtilSetResourceServiceEnvironment</b> calls  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a> and stores the resulting environment block in a registry entry for the service. For more information about the effects of the environment block, see  <b>ResUtilGetEnvironmentWithNetName</b>.

If your resource DLL manages a service, create a worker thread and use  <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceservicestartparameters">ResUtilSetResourceServiceStartParameters</a> and  <b>ResUtilSetResourceServiceEnvironment</b> when bringing the service online.

Do not call  <b>ResUtilSetResourceServiceEnvironment</b> from any resource DLL entry point function.  <b>ResUtilSetResourceServiceEnvironment</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>