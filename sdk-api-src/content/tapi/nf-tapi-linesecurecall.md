---
UID: NF:tapi.lineSecureCall
title: lineSecureCall function
author: windows-sdk-content
description: The lineSecureCall function secures the call from any interruptions or interference that can affect the call's media stream.
old-location: tapi2\linesecurecall.htm
tech.root: tapi
ms.assetid: b12a5734-0638-4bb0-8f25-ca27d28e528b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linesecurecall, lineSecureCall, lineSecureCall function [TAPI 2.2], tapi/lineSecureCall, tapi2.linesecurecall"
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
 - lineSecureCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSecureCall function


## -description


The 
<b>lineSecureCall</b> function secures the call from any interruptions or interference that can affect the call's media stream.


## -parameters




### -param hCall

Handle to the call to be secured. The application must be an owner of the call. The call state of <i>hCall</i> can be any state.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.




## -remarks



A call can be secured to avoid interference. For example, in an analog environment, call-waiting tones can destroy a fax or modem session on the original call. The 
<b>lineSecureCall</b> function allows an existing call to be secured. The 
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> function provides the option to secure the call from the time of call setup. The securing of a call remains in effect for the duration of the call.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/0a3be209-e3ff-4177-abb2-ad0facbdf569">Secure a Session overview</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>
 

 

