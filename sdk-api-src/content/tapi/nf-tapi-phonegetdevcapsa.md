---
UID: NF:tapi.phoneGetDevCapsA
title: phoneGetDevCapsA function (tapi.h)
description: The phoneGetDevCaps function queries a specified phone device to determine its telephony capabilities. (phoneGetDevCapsA)
helpviewer_keywords: ["phoneGetDevCapsA", "tapi/phoneGetDevCapsA"]
old-location: tapi2\phonegetdevcaps.htm
tech.root: tapi3
ms.assetid: 7bfef6d7-d5fd-4887-afb8-b1d850df050d
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetdevcaps, phoneGetDevCaps, phoneGetDevCaps function [TAPI 2.2], phoneGetDevCapsA, phoneGetDevCapsW, tapi/phoneGetDevCaps, tapi/phoneGetDevCapsA, tapi/phoneGetDevCapsW, tapi2.phonegetdevcaps
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneGetDevCapsW (Unicode) and phoneGetDevCapsA (ANSI)
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
 - phoneGetDevCapsA
 - tapi/phoneGetDevCapsA
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
 - phoneGetDevCaps
 - phoneGetDevCapsA
 - phoneGetDevCapsW
---

# phoneGetDevCapsA function


## -description

The 
<b>phoneGetDevCaps</b> function queries a specified phone device to determine its telephony capabilities.

## -parameters

### -param hPhoneApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the phone device to be queried.

### -param dwAPIVersion

Version number of the Telephony API to be used. The high-order word contains the major version number; the low-order word contains the minor version number. This number is obtained with the function 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>.

### -param dwExtVersion

Version number of the service provider-specific extensions to be used. This number is obtained with the function 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>. It can be left zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; the low-order word contains the minor version number.

### -param lpPhoneCaps

Pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>. Upon successful completion of the request, this structure is filled with phone device capabilities information.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_INVALPOINTER, PHONEERR_BADDEVICEID, PHONEERR_OPERATIONFAILED, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_NOMEM, PHONEERR_STRUCTURETOOSMALL, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODRIVER, PHONEERR_UNINITIALIZED, PHONEERR_NODEVICE.

## -remarks

Before using 
<b>phoneGetDevCaps</b>, the application must negotiate the TAPI version number to use (see 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>) and, optionally, the extension version to use (see 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>).

TAPI and extension version numbers are those under which TAPI, Telephony DLL, and service provider must operate. If version ranges do not overlap, the application and API or service-provider versions are incompatible and an error is returned.





> [!NOTE]
> The tapi.h header defines phoneGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>
