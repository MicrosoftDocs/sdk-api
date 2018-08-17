---
UID: NF:resapi.ResUtilStartResourceService
title: ResUtilStartResourceService function
author: windows-sdk-content
description: Starts a service. The PRESUTIL_START_RESOURCE_SERVICE type defines a pointer to this function.
old-location: mscs\resutilstartresourceservice.htm
old-project: mscs
ms.assetid: 0c8a80d7-0291-4ed5-af44-67c0c251dc84
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRESUTIL_START_RESOURCE_SERVICE, PRESUTIL_START_RESOURCE_SERVICE function [Failover Cluster], ResUtilStartResourceService, ResUtilStartResourceService function [Failover Cluster], _wolf_resutilstartresourceservice, mscs.resutilstartresourceservice, resapi/PRESUTIL_START_RESOURCE_SERVICE, resapi/ResUtilStartResourceService
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
 - ResUtilStartResourceService
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
---

# ResUtilStartResourceService function


## -description


Starts a <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">service</a>. The <b>PRESUTIL_START_RESOURCE_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to start.


### -param phServiceHandle [out]

Optional pointer to a handle in which the handle to the started service is returned. This handle must be closed either by a call to the cluster utility function  <a href="https://msdn.microsoft.com/22be9285-7db6-43dc-bf41-08187bbefc41">ResUtilStopService</a> or the function  <a href="https://msdn.microsoft.com/6cf25994-4939-4aff-af38-5ffc8fc606ae">CloseServiceHandle</a>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The  <b>ResUtilStartResourceService</b> utility function encapsulates the necessary calls to the service control manager, providing a convenient way to start services in the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. Using  <b>ResUtilStartResourceService</b> is optional. If the service to be started requires specific access restrictions or other special handling, use the service control manager functions instead.




## -see-also




<a href="https://msdn.microsoft.com/22be9285-7db6-43dc-bf41-08187bbefc41">ResUtilStopService</a>
 

 

