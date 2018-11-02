---
UID: NF:tapi.lineUnparkW
title: lineUnparkW function
author: windows-sdk-content
description: The lineUnpark function retrieves the call parked at the specified address and returns a call handle for it.
old-location: tapi2\lineunpark.htm
tech.root: tapi
ms.assetid: 9262ab44-eac7-43e2-a0ec-dceea0838b09
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_tapi2_lineunpark, lineUnpark, lineUnpark function [TAPI 2.2], lineUnparkA, lineUnparkW, tapi/lineUnpark, tapi/lineUnparkA, tapi/lineUnparkW, tapi2.lineunpark"
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
req.unicode-ansi: lineUnparkW (Unicode) and lineUnparkA (ANSI)
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
 - lineUnpark
 - lineUnparkA
 - lineUnparkW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineUnparkW function


## -description


The 
<b>lineUnpark</b> function retrieves the call parked at the specified address and returns a call handle for it.


## -parameters




### -param hLine

Handle to the open line device on which a call is to be unparked.


### -param dwAddressID

Address on <i>hLine</i> at which the unpark is to be originated. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param lphCall

Pointer to the location of type HCALL where the handle to the unparked call is returned. This handle is unrelated to any other handle that might have been previously associated with the retrieved call, such as the handle that might have been associated with the call when it was originally parked. The application is the initial sole owner of this call.


### -param lpszDestAddress

Pointer to a null-terminated character buffer that contains the address where the call is parked. The address is in standard dialable address format.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

