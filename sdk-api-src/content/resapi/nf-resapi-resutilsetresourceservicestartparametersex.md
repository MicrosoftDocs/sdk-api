---
UID: NF:resapi.ResUtilSetResourceServiceStartParametersEx
title: ResUtilSetResourceServiceStartParametersEx function (resapi.h)
description: Adjusts the start parameters of a specified service so that it operates correctly as a cluster resource. It must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX","PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX function [Failover Cluster]","ResUtilSetResourceServiceStartParametersEx","ResUtilSetResourceServiceStartParametersEx function [Failover Cluster]","mscs.resutilsetresourceservicestartparametersex","resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX","resapi/ResUtilSetResourceServiceStartParametersEx"]
old-location: mscs\resutilsetresourceservicestartparametersex.htm
tech.root: MsCS
ms.assetid: 12F1AD70-4B6C-4920-855C-C55C8F423C69
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX, PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX function [Failover Cluster], ResUtilSetResourceServiceStartParametersEx, ResUtilSetResourceServiceStartParametersEx function [Failover Cluster], mscs.resutilsetresourceservicestartparametersex, resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX, resapi/ResUtilSetResourceServiceStartParametersEx
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ResUtilSetResourceServiceStartParametersEx
 - resapi/ResUtilSetResourceServiceStartParametersEx
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
 - ResUtilSetResourceServiceStartParametersEx
---

# ResUtilSetResourceServiceStartParametersEx function


## -description

Adjusts the start parameters of a specified <a href="/previous-versions/windows/desktop/mscs/s-gly">service</a> so that it  operates  correctly as a cluster  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. It must be called from a  <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX</b> type defines a pointer to this function.

## -parameters

### -param pszServiceName [in]

A pointer to a null-terminated Unicode string that specifies  the name of the service.

### -param schSCMHandle [in]

A handle to the Service Control Manager (SCM) or <b>NULL</b>. If <b>NULL</b>, the function  attempts to open a handle to the SCM.

### -param phService [in, out]

On input, a <b>NULL</b> service handle. On output, handle to the specified service if the call was successful; otherwise <b>NULL</b>.

### -param dwDesiredAccess [in]

The requested access privileges. This  might  be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0),  an undefined error might  be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceservicestartparameters">ResUtilSetResourceServiceStartParameters</a>.

### -param pfnLogEvent [in]

A pointer to the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function of the resource DLL that manages  the service.

### -param hResourceHandle [in]

A resource handle that is required by the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function. Use the handle that is passed to the DLL in the  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>ResUtilSetResourceServiceStartParametersEx</b> verifies that the service is not disabled, changes the service configuration to manual start, and prevents the service from restarting in response to failure. This  enables  the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and the resource DLL to control the service.

If your resource DLL manages a service, use  <b>ResUtilSetResourceServiceStartParametersEx</b> and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceserviceenvironment">ResUtilSetResourceServiceEnvironment</a> before you  bring the service online.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceservicestartparameters">ResUtilSetResourceServiceStartParameters</a>



<a href="/previous-versions/windows/desktop/mscs/service-utility-functions">Service Utility Functions</a>