---
UID: NF:resapi.ResUtilVerifyResourceService
title: ResUtilVerifyResourceService function
author: windows-sdk-content
description: Verifies that a named service is starting or currently running. The PRESUTIL_VERIFY_RESOURCE_SERVICE type defines a pointer to this function.
old-location: mscs\resutilverifyresourceservice.htm
tech.root: mscs
ms.assetid: 452f4e83-74a6-4830-b244-599e9dc5c854
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PRESUTIL_VERIFY_RESOURCE_SERVICE, PRESUTIL_VERIFY_RESOURCE_SERVICE function [Failover Cluster], ResUtilVerifyResourceService, ResUtilVerifyResourceService function [Failover Cluster], _wolf_resutilverifyresourceservice, mscs.resutilverifyresourceservice, resapi/PRESUTIL_VERIFY_RESOURCE_SERVICE, resapi/ResUtilVerifyResourceService
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ResUtilVerifyResourceService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilVerifyResourceService function


## -description


Verifies that a named <a href="s_gly.htm">service</a> is starting or currently running. The <b>PRESUTIL_VERIFY_RESOURCE_SERVICE</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Null-terminated Unicode string containing the name of the service to verify.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.



