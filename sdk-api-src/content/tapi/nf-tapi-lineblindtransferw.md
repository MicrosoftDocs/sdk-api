---
UID: NF:tapi.lineBlindTransferW
title: lineBlindTransferW function (tapi.h)
description: The lineBlindTransfer function performs a blind or single-step transfer of the specified call to the specified destination address.helpviewer_keywords: ["_tapi2_lineblindtransfer","lineBlindTransfer","lineBlindTransfer function [TAPI 2.2]","lineBlindTransferA","lineBlindTransferW","tapi/lineBlindTransfer","tapi/lineBlindTransferA","tapi/lineBlindTransferW","tapi2.lineblindtransfer"]
old-location: tapi2\lineblindtransfer.htm
tech.root: Tapi
ms.assetid: c1997933-475e-4bcd-be44-ad92a2a678eb
ms.date: 12/05/2018
ms.keywords: _tapi2_lineblindtransfer, lineBlindTransfer, lineBlindTransfer function [TAPI 2.2], lineBlindTransferA, lineBlindTransferW, tapi/lineBlindTransfer, tapi/lineBlindTransferA, tapi/lineBlindTransferW, tapi2.lineblindtransfer
f1_keywords:
- tapi/lineBlindTransfer
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# lineBlindTransferW function


## -description


The 
<b>lineBlindTransfer</b> function performs a blind or single-step transfer of the specified call to the specified destination address.


## -parameters




### -param hCall

Handle to the call to be transferred. The application must be an owner of this call. The call state of <i>hCall</i> must be <i>connected</i>.


#### - lpszDestAddressW

Pointer to a null-terminated string identifying where the call is to be transferred to. The destination address uses the standard dialable number format.


### -param dwCountryCode

Country or region code of the destination. This is used by the implementation to select the call progress protocols for the destination address. If a value of 0 is specified, a default call-progress protocol defined by the service provider is used.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCOUNTRYCODE, LINEERR_INVALCALLSTATE, LINEERR_INVALPOINTER, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_NOTOWNER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALADDRESS, LINEERR_UNINITIALIZED, LINEERR_ADDRESSBLOCKED, LINEERR_OPERATIONFAILED.




## -remarks



If LINEERR_INVALADDRESS is returned, no dialing occurs.

Blind transfer differs from a consultation transfer in that no consultation call is made visible to the application. After the blind transfer successfully completes, the specified call is typically cleared from the application's line, and it transitions to the <i>idle</i> state.

The application's call handle remains valid after the transfer has completed. The application must deallocate its handle using 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linedeallocatecall">lineDeallocateCall</a> when it is no longer interested in the transferred call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/transfer-ovr">Transfer overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linedeallocatecall">lineDeallocateCall</a>
 

 

