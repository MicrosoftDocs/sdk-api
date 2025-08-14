---
UID: NF:tapi.lineGetDevCapsW
title: lineGetDevCapsW function (tapi.h)
description: The lineGetDevCapsW (Unicode) function (tapi.h) queries a specified line device to determine its telephony capabilities.
helpviewer_keywords: ["_tapi2_linegetdevcaps", "lineGetDevCaps", "lineGetDevCaps function [TAPI 2.2]", "lineGetDevCapsW", "tapi/lineGetDevCaps", "tapi/lineGetDevCapsW", "tapi2.linegetdevcaps"]
old-location: tapi2\linegetdevcaps.htm
tech.root: tapi3
ms.assetid: c0900c5b-8791-4653-8bfc-d32e51d10c50
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetdevcaps, lineGetDevCaps, lineGetDevCaps function [TAPI 2.2], lineGetDevCapsA, lineGetDevCapsW, tapi/lineGetDevCaps, tapi/lineGetDevCapsA, tapi/lineGetDevCapsW, tapi2.linegetdevcaps
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetDevCapsW (Unicode) and lineGetDevCapsA (ANSI)
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
 - lineGetDevCapsW
 - tapi/lineGetDevCapsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineGetDevCaps
 - lineGetDevCapsA
 - lineGetDevCapsW
---

# lineGetDevCapsW function


## -description

The 
<b>lineGetDevCaps</b> function queries a specified line device to determine its telephony capabilities. The returned information is valid for all addresses on the line device.

## -parameters

### -param hLineApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the line device to be queried.

### -param dwAPIVersion

Version number of the Telephony API to be used. The high-order word contains the major version number; the low-order word contains the minor version number. This number is obtained by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>.

### -param dwExtVersion

Version number of the service provider-specific extensions to be used. This number is obtained by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateextversion">lineNegotiateExtVersion</a>. It can be left zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; the low-order word contains the minor version number.

### -param lpLineDevCaps

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>. Upon successful completion of the request, this structure is filled with line device capabilities information. Prior to calling 
<b>lineGetDevCaps</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONFAILED, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALAPPHANDLE, LINEERR_STRUCTURETOOSMALL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NODRIVER, LINEERR_OPERATIONUNAVAIL, LINEERR_NODEVICE.

## -remarks

Before using 
<b>lineGetDevCaps</b>, the application must negotiate the API version number to use, and, if desired, the extension version to use.

The API and extension version numbers are those under which TAPI and the service provider must operate. If version ranges do not overlap, the application, API, or service-provider versions are incompatible and an error is returned.

One of the members in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure returned by this function contains the number of addresses assigned to the specified line device. The actual address identifiers used to reference individual addresses vary from zero to one less than the returned number. The capabilities of each address can be different. Use 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a> for each available &lt;<i>dwDeviceID</i>, <i>dwAddressID</i>&gt; combination to determine the exact capabilities of each address. Note that an address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.





> [!NOTE]
> The tapi.h header defines lineGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateextversion">lineNegotiateExtVersion</a>
