---
UID: NF:tapi.phoneNegotiateAPIVersion
title: phoneNegotiateAPIVersion function (tapi.h)
description: The phoneNegotiateAPIVersion allows an application to negotiate an API version to use for the specified phone device.
helpviewer_keywords: ["_tapi2_phonenegotiateapiversion","phoneNegotiateAPIVersion","phoneNegotiateAPIVersion function [TAPI 2.2]","tapi/phoneNegotiateAPIVersion","tapi2.phonenegotiateapiversion"]
old-location: tapi2\phonenegotiateapiversion.htm
tech.root: tapi3
ms.assetid: 50c2c15c-459f-451b-9b79-9118acc81c8c
ms.date: 12/05/2018
ms.keywords: _tapi2_phonenegotiateapiversion, phoneNegotiateAPIVersion, phoneNegotiateAPIVersion function [TAPI 2.2], tapi/phoneNegotiateAPIVersion, tapi2.phonenegotiateapiversion
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
 - phoneNegotiateAPIVersion
 - tapi/phoneNegotiateAPIVersion
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
 - phoneNegotiateAPIVersion
---

# phoneNegotiateAPIVersion function


## -description

The 
<b>phoneNegotiateAPIVersion</b> allows an application to negotiate an API version to use for the specified phone device.

## -parameters

### -param hPhoneApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the phone device to be queried.

### -param dwAPILowVersion

Least recent API version the application is compliant with. The high-order word is the major version number, the low-order word is the minor version number.

### -param dwAPIHighVersion

Most recent API version the application is compliant with. The high-order word is the major version number, the low-order word is the minor version number.

### -param lpdwAPIVersion

Pointer to a <b>DWORD</b> in which the API version number that was negotiated will be returned. If negotiation succeeds, this number is in the range <i>dwAPILowVersion</i> to <i>dwAPIHighVersion</i>.

### -param lpExtensionID

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneextensionid">PHONEEXTENSIONID</a>. If the service provider for the specified <i>dwDeviceID</i> parameter supports provider-specific extensions, this structure is filled with the extension identifier of these extensions when negotiation succeeds. This structure contains all zeros if the line provides no extensions. An application can ignore the returned parameter if it does not use extensions.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_BADDEVICEID, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NODRIVER, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_UNINITIALIZED, PHONEERR_NODEVICE.

## -remarks

The 
<b>phoneNegotiateAPIVersion</b> function is used to negotiate the API version number to use with the specified phone device. It returns the extension identifier supported by the phone device, or zeros if no extensions are provided.

If the application wants to use the extensions defined by the returned extension identifier, it must call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a> to negotiate the extension version to use.

Use 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a> to determine the number of phone devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of phone devices present.

The API version number negotiated is that under which TAPI can operate. If version ranges do not overlap, the application, API, or service-provider versions are incompatible and an error is returned.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phoneextensionid">PHONEEXTENSIONID</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/tapi-versioning">TAPI Versioning</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateextversion">phoneNegotiateExtVersion</a>