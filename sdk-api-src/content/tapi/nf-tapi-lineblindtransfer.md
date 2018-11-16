---
UID: NF:tapi.lineBlindTransfer
title: lineBlindTransfer function
author: windows-sdk-content
description: The lineBlindTransfer function performs a blind or single-step transfer of the specified call to the specified destination address.
old-location: tapi2\lineblindtransfer.htm
tech.root: Tapi
ms.assetid: c1997933-475e-4bcd-be44-ad92a2a678eb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_tapi2_lineblindtransfer, lineBlindTransfer, lineBlindTransfer function [TAPI 2.2], lineBlindTransferA, lineBlindTransferW, tapi/lineBlindTransfer, tapi/lineBlindTransferA, tapi/lineBlindTransferW, tapi2.lineblindtransfer"
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
req.unicode-ansi: lineBlindTransferW (Unicode) and lineBlindTransferA (ANSI)
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
 - lineBlindTransfer
 - lineBlindTransferA
 - lineBlindTransferW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- lineBlindTransfer
: 
---

# lineBlindTransfer function


## -description


The 
<b>lineBlindTransfer</b> function performs a blind or single-step transfer of the specified call to the specified destination address.


## -parameters




### -param hCall

Handle to the call to be transferred. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>connected</i>.


### -param lpszDestAddress

TBD


### -param dwCountryCode

Country or region code of the destination. This is used by the implementation to select the call progress protocols for the destination address. If a value of 0 is specified, a default call-progress protocol defined by the service provider is used.


#### - lpszDestAddressW

Pointer to a null-terminated string identifying where the call is to be transferred to. The destination address uses the standard dialable number format.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCOUNTRYCODE, LINEERR_INVALCALLSTATE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_NOTOWNER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALADDRESS, LINEERR_UNINITIALIZED, LINEERR_ADDRESSBLOCKED, LINEERR_OPERATIONFAILED.




## -remarks



If LINEERR_INVALADDRESS is returned, no dialing occurs.

Blind transfer differs from a consultation transfer in that no consultation call is made visible to the application. After the blind transfer successfully completes, the specified call is typically cleared from the application's line, and it transitions to the <i>idle</i> state.

The application's call handle remains valid after the transfer has completed. The application must deallocate its handle using 
<a href="https://msdn.microsoft.com/a695ee19-e371-4126-b438-62bf52179cba">lineDeallocateCall</a> when it is no longer interested in the transferred call.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/b1027f09-74e1-4da8-b718-bb55a56dda1d">Transfer overview</a>



<a href="https://msdn.microsoft.com/a695ee19-e371-4126-b438-62bf52179cba">lineDeallocateCall</a>
 

 

