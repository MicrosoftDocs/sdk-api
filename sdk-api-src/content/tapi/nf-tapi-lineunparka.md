---
UID: NF:tapi.lineUnparkA
title: lineUnparkA function (tapi.h)
description: The lineUnpark function retrieves the call parked at the specified address and returns a call handle for it. (lineUnparkA)
helpviewer_keywords: ["lineUnparkA", "tapi/lineUnparkA"]
old-location: tapi2\lineunpark.htm
tech.root: tapi3
ms.assetid: 9262ab44-eac7-43e2-a0ec-dceea0838b09
ms.date: 12/05/2018
ms.keywords: _tapi2_lineunpark, lineUnpark, lineUnpark function [TAPI 2.2], lineUnparkA, lineUnparkW, tapi/lineUnpark, tapi/lineUnparkA, tapi/lineUnparkW, tapi2.lineunpark
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineUnparkA
 - tapi/lineUnparkA
dev_langs:
 - c++
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
---

# lineUnparkA function


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
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineUnpark as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
