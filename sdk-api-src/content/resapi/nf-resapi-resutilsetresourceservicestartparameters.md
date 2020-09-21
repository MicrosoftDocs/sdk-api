---
UID: NF:resapi.ResUtilSetResourceServiceStartParameters
title: ResUtilSetResourceServiceStartParameters function (resapi.h)
description: Adjusts the start parameters of a specified service so that it will operate correctly as a cluster resource. It must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS","PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS function [Failover Cluster]","ResUtilSetResourceServiceStartParameters","ResUtilSetResourceServiceStartParameters function [Failover Cluster]","_wolf_resutilsetresourceservicestartparameters","mscs.resutilsetresourceservicestartparameters","resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS","resapi/ResUtilSetResourceServiceStartParameters"]
old-location: mscs\resutilsetresourceservicestartparameters.htm
tech.root: MsCS
ms.assetid: 5400ed27-4299-470c-bfce-bc91d09f1708
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS, PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS function [Failover Cluster], ResUtilSetResourceServiceStartParameters, ResUtilSetResourceServiceStartParameters function [Failover Cluster], _wolf_resutilsetresourceservicestartparameters, mscs.resutilsetresourceservicestartparameters, resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS, resapi/ResUtilSetResourceServiceStartParameters
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
 - ResUtilSetResourceServiceStartParameters
 - resapi/ResUtilSetResourceServiceStartParameters
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
 - ResUtilSetResourceServiceStartParameters
---

# ResUtilSetResourceServiceStartParameters function


## -description

Adjusts the start parameters of a specified <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a> so that it will operate correctly as a cluster  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. It must be called from a  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

Pointer to a null-terminated Unicode string specifying the name of the service.

### -param schSCMHandle [in]

Handle to the Service Control Manager (SCM) or <b>NULL</b>. If <b>NULL</b>, the function will attempt to open a handle to the SCM.

### -param phService [in, out]

On input, a <b>NULL</b> service handle. On output, handle to the specified service if the call was successful, otherwise <b>NULL</b>.

### -param pfnLogEvent [in]

Pointer to the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function of the resource DLL managing the service.

### -param hResourceHandle [in]

Resource handle required by the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function. Use the handle passed to the DLL in the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>ResUtilSetResourceServiceStartParameters</b> verifies that the service is not disabled, changes the service configuration to manual start and prevents the service from restarting in response to failure. This allows the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and the resource DLL to control the service.

If your resource DLL manages a service, use  <b>ResUtilSetResourceServiceStartParameters</b> and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceserviceenvironment">ResUtilSetResourceServiceEnvironment</a> before bringing the service online.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceserviceenvironment">ResUtilSetResourceServiceEnvironment</a>