---
UID: NF:tapi.lineRedirect
title: lineRedirect function
author: windows-sdk-content
description: The lineRedirect function redirects the specified offering call to the specified destination address.
old-location: tapi2\lineredirect.htm
tech.root: tapi
ms.assetid: 014465af-26a7-451e-9d32-2e020d1043b0
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_lineredirect, lineRedirect, lineRedirect function [TAPI 2.2], lineRedirectA, lineRedirectW, tapi/lineRedirect, tapi/lineRedirectA, tapi/lineRedirectW, tapi2.lineredirect"
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
req.unicode-ansi: lineRedirectW (Unicode) and lineRedirectA (ANSI)
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
 - lineRedirect
 - lineRedirectA
 - lineRedirectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineRedirect function


## -description


The 
<b>lineRedirect</b> function redirects the specified offering call to the specified destination address.


## -parameters




### -param hCall

Handle to the call to be redirected. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>offering</i>.


### -param lpszDestAddress

Pointer to the destination address. This follows the standard dialable number format.


### -param dwCountryCode

Country/region code of the party the call is redirected to. If a value of 0 is specified, a default is used by the implementation.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_NOTOWNER, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALCOUNTRYCODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



Call redirect allows an application to deflect an offering call to another address without first answering the call. Call redirect differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information. It differs from call transfer in that transferring a call requires the call first be answered.

After a call has been successfully redirected, the call typically transitions to idle.

Besides redirecting an incoming call, an application may have the option to accept the call using 
<a href="https://msdn.microsoft.com/185f129a-ba8c-496b-ab1a-ba22e5928c54">lineAccept</a>, reject the call using 
<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>, or answer the call using 
<a href="https://msdn.microsoft.com/dd51991c-c044-4b88-8f97-9e0ae701a2a5">lineAnswer</a>. The availability of these operations is dependent on device capabilities.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/b52cd5c2-fdd6-4240-b07b-b22733a89d27">Redirect overview</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/185f129a-ba8c-496b-ab1a-ba22e5928c54">lineAccept</a>



<a href="https://msdn.microsoft.com/dd51991c-c044-4b88-8f97-9e0ae701a2a5">lineAnswer</a>



<a href="https://msdn.microsoft.com/ce1f1dbb-287b-483a-9e7e-87af0d07e4e4">lineDrop</a>
 

 

