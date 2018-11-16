---
UID: NF:tapi.phoneClose
title: phoneClose function
author: windows-sdk-content
description: The phoneClose function closes the specified open phone device.
old-location: tapi2\phoneclose.htm
tech.root: Tapi
ms.assetid: 9e5e66c6-a8d2-4e0a-a400-17f0a3637f63
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_tapi2_phoneclose, phoneClose, phoneClose function [TAPI 2.2], tapi/phoneClose, tapi2.phoneclose"
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
 - phoneClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- phoneClose
: 
---

# phoneClose function


## -description


The 
<b>phoneClose</b> function closes the specified open phone device.


## -parameters




### -param hPhone

Handle to the open phone device to be closed. If the function succeeds, the handle is no longer valid.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_OPERATIONFAILED, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -remarks



After the open phone device has been successfully closed, the implementation sends a 
<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a> message to the application. These messages can also be sent unsolicited as a result of the phone device being reclaimed somehow. An application should therefore be prepared to handle these unsolicited close messages. At the time the phone device is closed, any outstanding asynchronous replies are suppressed.




## -see-also




<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

