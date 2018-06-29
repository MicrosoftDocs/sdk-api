---
UID: NC:resapi.PRESUTIL_VERIFY_SERVICE
title: PRESUTIL_VERIFY_SERVICE
author: windows-sdk-content
description: Checks if a service identified by a handle is starting or currently running. The PRESUTIL_VERIFY_SERVICE type defines a pointer to this function.
old-location: mscs\resutilverifyservice.htm
old-project: MsCS
ms.assetid: a846d09f-9fa3-4749-86c8-b57e69b297dd
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_VERIFY_SERVICE, PRESUTIL_VERIFY_SERVICE callback, PRESUTIL_VERIFY_SERVICE callback function [Failover Cluster], _wolf_resutilverifyservice, mscs.resutilverifyservice, resapi/PRESUTIL_VERIFY_SERVICE
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
 - PRESUTIL_VERIFY_SERVICE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_VERIFY_SERVICE callback function


## -description


Checks if a <a href="https://msdn.microsoft.com/library/windows/hardware/mt269769">service</a> identified by a handle is starting or currently running. The <b>PRESUTIL_VERIFY_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param hServiceHandle [in]

Handle of the service to verify.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.



