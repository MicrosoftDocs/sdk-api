---
UID: NF:resapi.ResUtilStopResourceService
title: ResUtilStopResourceService function
author: windows-sdk-content
description: Stops a named service. The PRESUTIL_STOP_RESOURCE_SERVICE type defines a pointer to this function.
old-location: mscs\resutilstopresourceservice.htm
old-project: mscs
ms.assetid: 25e8417d-d314-4987-bdb2-7740793e4ac2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRESUTIL_STOP_RESOURCE_SERVICE, PRESUTIL_STOP_RESOURCE_SERVICE function [Failover Cluster], ResUtilStopResourceService, ResUtilStopResourceService function [Failover Cluster], _wolf_resutilstopresourceservice, mscs.resutilstopresourceservice, resapi/PRESUTIL_STOP_RESOURCE_SERVICE, resapi/ResUtilStopResourceService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilStopResourceService
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
---

# ResUtilStopResourceService function


## -description


Stops a named <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">service</a>. The <b>PRESUTIL_STOP_RESOURCE_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to stop.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -see-also




<a href="https://msdn.microsoft.com/0c8a80d7-0291-4ed5-af44-67c0c251dc84">ResUtilStartResourceService</a>
 

 

