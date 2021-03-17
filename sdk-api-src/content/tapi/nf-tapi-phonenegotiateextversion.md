---
UID: NF:tapi.phoneNegotiateExtVersion
title: phoneNegotiateExtVersion function (tapi.h)
description: The phoneNegotiateExtVersion function allows an application to negotiate an extension version to use with the specified phone device. This operation need not be called if the application does not support extensions.
helpviewer_keywords: ["_tapi2_phonenegotiateextversion","phoneNegotiateExtVersion","phoneNegotiateExtVersion function [TAPI 2.2]","tapi/phoneNegotiateExtVersion","tapi2.phonenegotiateextversion"]
old-location: tapi2\phonenegotiateextversion.htm
tech.root: tapi3
ms.assetid: f62aa1da-7256-400a-998d-4c24d01989ec
ms.date: 12/05/2018
ms.keywords: _tapi2_phonenegotiateextversion, phoneNegotiateExtVersion, phoneNegotiateExtVersion function [TAPI 2.2], tapi/phoneNegotiateExtVersion, tapi2.phonenegotiateextversion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phoneNegotiateExtVersion
 - tapi/phoneNegotiateExtVersion
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
 - phoneNegotiateExtVersion
---

# phoneNegotiateExtVersion function


## -description

The 
<b>phoneNegotiateExtVersion</b> function allows an application to negotiate an extension version to use with the specified phone device. This operation need not be called if the application does not support extensions.

## -parameters

### -param hPhoneApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the phone device to be queried.

### -param dwAPIVersion

API version number that was negotiated for the specified phone device using 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>.

### -param dwExtLowVersion

Least recent extension version of the extension identifier returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a> that the application is compliant with. The high-order word is the major version number; the low-order word is the minor version number.

### -param dwExtHighVersion

Most recent extension version of the extension identifier returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a> that the application is compliant with. The high-order word is the major version number; the low-order word is the minor version number.

### -param lpdwExtVersion

Pointer to a <b>DWORD</b> in which the extension version number that was negotiated is returned. If negotiation succeeds, this number is in the range <i>dwExtLowVersion</i> to <i>dwExtHighVersion</i>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_BADDEVICEID, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NODRIVER, PHONEERR_NOMEM, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_UNINITIALIZED, PHONEERR_INVALPOINTER, PHONEERR_NODEVICE.

## -remarks

The 
<b>phoneNegotiateExtVersion</b> function is used to negotiate the API version number to use. It returns the extension identifier supported by the phone device, or zeros if no extensions are provided.

In order for the application to use the extensions defined by the returned extension identifier, it must call 
<b>phoneNegotiateExtVersion</b> to negotiate the extension version to use.

Use 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a> to determine the number of phone devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of phone devices present.

The extension version number negotiated is that under which the application and service provider must both operate. If version ranges do not overlap, the application and service-provider versions are incompatible and an error is returned.

## -see-also

<a href="/windows/desktop/Tapi/extended-telephony-services-reference">Extended Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>