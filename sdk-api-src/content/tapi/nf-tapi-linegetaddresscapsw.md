---
UID: NF:tapi.lineGetAddressCapsW
title: lineGetAddressCapsW function (tapi.h)
description: The lineGetAddressCapsW (Unicode) function (tapi.h) queries the specified address on the specified line device to determine its telephony capabilities.
helpviewer_keywords: ["_tapi2_linegetaddresscaps", "lineGetAddressCaps", "lineGetAddressCaps function [TAPI 2.2]", "lineGetAddressCapsW", "tapi/lineGetAddressCaps", "tapi/lineGetAddressCapsW", "tapi2.linegetaddresscaps"]
old-location: tapi2\linegetaddresscaps.htm
tech.root: tapi3
ms.assetid: 08cdea8a-5b36-428c-b90f-8741ae5f3205
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetaddresscaps, lineGetAddressCaps, lineGetAddressCaps function [TAPI 2.2], lineGetAddressCapsA, lineGetAddressCapsW, tapi/lineGetAddressCaps, tapi/lineGetAddressCapsA, tapi/lineGetAddressCapsW, tapi2.linegetaddresscaps
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAddressCapsW (Unicode) and lineGetAddressCapsA (ANSI)
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
 - lineGetAddressCapsW
 - tapi/lineGetAddressCapsW
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
 - lineGetAddressCaps
 - lineGetAddressCapsA
 - lineGetAddressCapsW
---

# lineGetAddressCapsW function


## -description

The 
<b>lineGetAddressCaps</b> function queries the specified address on the specified line device to determine its telephony capabilities.

## -parameters

### -param hLineApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Line device containing the address to be queried.

### -param dwAddressID

Address on the given line device whose capabilities are to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param dwAPIVersion

Version number of the Telephony API to be used. The high-order word contains the major version number; the low-order word contains the minor version number. This number is obtained by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>.

### -param dwExtVersion

Version number of the service provider-specific extensions to be used. This number can be set to zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; and the low-order word contains the minor version number.

### -param lpAddressCaps

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>. Upon successful completion of the request, this structure is filled with address capabilities information. Prior to calling 
<b>lineGetAddressCaps</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONFAILED, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALAPPHANDLE, LINEERR_UNINITIALIZED, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_NODEVICE.

## -remarks

Valid address identifiers range from zero to one less than the number of addresses returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>. The version number to be supplied is the version number that was returned as part of the line's device capabilities by 
<b>lineGetDevCaps</b>.





> [!NOTE]
> The tapi.h header defines lineGetAddressCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>
