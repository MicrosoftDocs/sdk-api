---
UID: NF:tapi.lineShutdown
title: lineShutdown function (tapi.h)
author: windows-sdk-content
description: The lineShutdown function shuts down the application's usage of the line abstraction of the API.
old-location: tapi2\lineshutdown.htm
tech.root: Tapi
ms.assetid: d512508a-fb6a-41ec-a80d-f625abfdd184
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_lineshutdown, lineShutdown, lineShutdown function [TAPI 2.2], tapi/lineShutdown, tapi2.lineshutdown"
ms.topic: function
f1_keywords: 
 - "tapi/lineShutdown"
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineShutdown function


## -description


The 
<b>lineShutdown</b> function shuts down the application's usage of the line abstraction of the API.


## -parameters




### -param hLineApp

Application's usage handle for the line API.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



If this function is called when the application has lines open or calls active, the call handles are deleted and TAPI automatically performs the equivalent of a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineclose">lineClose</a> on each open line. However, it is recommended that applications explicitly close all open lines before invoking 
<b>lineShutdown</b>. If shutdown is performed while asynchronous requests are outstanding, those requests are canceled.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineclose">lineClose</a>
 

 

