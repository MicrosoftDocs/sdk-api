---
UID: NF:tapi.lineGetAddressStatusA
title: lineGetAddressStatusA function (tapi.h)
description: The lineGetAddressStatus function allows an application to query the specified address for its current status. (lineGetAddressStatusA)
helpviewer_keywords: ["lineGetAddressStatusA", "tapi/lineGetAddressStatusA"]
old-location: tapi2\linegetaddressstatus.htm
tech.root: tapi3
ms.assetid: 8d747aa5-05cc-4426-9d46-24bce6b4af26
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetaddressstatus, lineGetAddressStatus, lineGetAddressStatus function [TAPI 2.2], lineGetAddressStatusA, lineGetAddressStatusW, tapi/lineGetAddressStatus, tapi/lineGetAddressStatusA, tapi/lineGetAddressStatusW, tapi2.linegetaddressstatus
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAddressStatusW (Unicode) and lineGetAddressStatusA (ANSI)
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
 - lineGetAddressStatusA
 - tapi/lineGetAddressStatusA
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
 - lineGetAddressStatus
 - lineGetAddressStatusA
 - lineGetAddressStatusW
---

# lineGetAddressStatusA function


## -description

The 
<b>lineGetAddressStatus</b> function allows an application to query the specified address for its current status.

## -parameters

### -param hLine

Handle to the open line device.

### -param dwAddressID

Address on the given open line device. This is the address to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param lpAddressStatus

Pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>. Prior to calling 
<b>lineGetAddressStatus</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>

## -remarks

> [!NOTE]
> The tapi.h header defines lineGetAddressStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
