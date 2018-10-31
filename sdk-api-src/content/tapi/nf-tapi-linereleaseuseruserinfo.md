---
UID: NF:tapi.lineReleaseUserUserInfo
title: lineReleaseUserUserInfo function
author: windows-sdk-content
description: The lineReleaseUserUserInfo function informs the service provider that the application has processed the user-user information contained in the LINECALLINFO structure.
old-location: tapi2\linereleaseuseruserinfo.htm
tech.root: tapi
ms.assetid: 35d41764-7ed6-4be3-8854-37444f2a44a8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_tapi2_linereleaseuseruserinfo, lineReleaseUserUserInfo, lineReleaseUserUserInfo function [TAPI 2.2], tapi/lineReleaseUserUserInfo, tapi2.linereleaseuseruserinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - lineReleaseUserUserInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineReleaseUserUserInfo function


## -description


The 
<b>lineReleaseUserUserInfo</b> function informs the service provider that the application has processed the user-user information contained in the 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure, and that subsequently received user-user information can now be written into that structure. The service provider sends a 
<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a> message indicating LINECALLINFOSTATE_USERUSERINFO when new information is available.


## -parameters




### -param hCall

Handle to the call. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.




## -remarks



The 
<b>lineReleaseUserUserInfo</b> function allows the application to control the flow of incoming user-user information on an ISDN connection. When a new, complete user-user information message is received, the service provider informs the application using a 
<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a> message (specifying LINECALLINFOSTATE_USERUSERINFO). Any number of applications can examine the information (using 
<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>), but the application owning the call controls when the information is released so that subsequent information can be reported. The service provider will not overwrite previous user-user information in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> with newer information until after 
<b>lineReleaseUserUserInfo</b> has been called. It is the responsibility of the service provider to buffer subsequently received user-user information until the previous information is released by the application owning the call.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e69722cb-9c45-4f1a-a855-64afa3c33276">lineGetCallInfo</a>
 

 

