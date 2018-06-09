---
UID: NC:resapi.PRESUTIL_STOP_SERVICE
title: PRESUTIL_STOP_SERVICE
author: windows-sdk-content
description: Stops a service identified by a handle. The PRESUTIL_STOP_SERVICE type defines a pointer to this function.
old-location: mscs\resutilstopservice.htm
old-project: MsCS
ms.assetid: 22be9285-7db6-43dc-bf41-08187bbefc41
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_STOP_SERVICE, PRESUTIL_STOP_SERVICE callback, PRESUTIL_STOP_SERVICE callback function [Failover Cluster], _wolf_resutilstopservice, mscs.resutilstopservice, resapi/PRESUTIL_STOP_SERVICE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_STOP_SERVICE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_STOP_SERVICE callback function


## -description


Stops a <a href="https://msdn.microsoft.com/library/windows/hardware/mt269769">service</a> identified by a handle. The <b>PRESUTIL_STOP_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param hServiceHandle [in]

Handle of the service to stop.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The  <i>ResUtilStopService</i> utility function closes the handle specified in <i>hServiceHandle</i> when it stops the service.



