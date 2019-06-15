---
UID: NF:resapi.ResUtilRemoveResourceServiceEnvironment
title: ResUtilRemoveResourceServiceEnvironment function (resapi.h)
author: windows-sdk-content
description: Removes the environment data from a service. This function must be called from a resource DLL. The PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT type defines a pointer to this function.
old-location: mscs\resutilremoveresourceserviceenvironment.htm
tech.root: MsCS
ms.assetid: e0e3ea2d-9cf2-40f6-a3a8-fdcacb63479c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT, PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT function [Failover Cluster], ResUtilRemoveResourceServiceEnvironment, ResUtilRemoveResourceServiceEnvironment function [Failover Cluster], mscs.resutilremoveresourceserviceenvironment, resapi/PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT, resapi/ResUtilRemoveResourceServiceEnvironment
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilRemoveResourceServiceEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilRemoveResourceServiceEnvironment function


## -description


Removes the environment data from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/s-gly">service</a>. This function must be called from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>. The <b>PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Pointer  to a null-terminated Unicode string  that contains the name of the service.


### -param pfnLogEvent [in]

Pointer to the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function of the resource DLL  that manages  the service.


### -param hResourceHandle [in]

Resource handle  that  the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a> entry point function  requires. Use the handle passed to the DLL in the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>
 

 

