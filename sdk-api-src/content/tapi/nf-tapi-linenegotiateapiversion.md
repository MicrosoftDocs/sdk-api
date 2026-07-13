---
UID: NF:tapi.lineNegotiateAPIVersion
title: lineNegotiateAPIVersion function (tapi.h)
description: The lineNegotiateAPIVersion function allows an application to negotiate an API version to use.
helpviewer_keywords: ["_tapi2_linenegotiateapiversion","lineNegotiateAPIVersion","lineNegotiateAPIVersion function [TAPI 2.2]","tapi/lineNegotiateAPIVersion","tapi2.linenegotiateapiversion"]
old-location: tapi2\linenegotiateapiversion.htm
tech.root: tapi3
ms.assetid: 71eb55de-281b-42a9-8d9b-7ded62cb006a
ms.date: 12/05/2018
ms.keywords: _tapi2_linenegotiateapiversion, lineNegotiateAPIVersion, lineNegotiateAPIVersion function [TAPI 2.2], tapi/lineNegotiateAPIVersion, tapi2.linenegotiateapiversion
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
 - lineNegotiateAPIVersion
 - tapi/lineNegotiateAPIVersion
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
 - lineNegotiateAPIVersion
---

# lineNegotiateAPIVersion function


## -description

The 
<b>lineNegotiateAPIVersion</b> function allows an application to negotiate an API version to use.

## -parameters

### -param hLineApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the line device to be queried.

### -param dwAPILowVersion

Earliest TAPI version with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.

### -param dwAPIHighVersion

Latest TAPI version with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.

### -param lpdwAPIVersion

Pointer to a variable that contains the TAPI version number that was negotiated. If negotiation succeeds, this number is in the range between <i>dwAPILowVersion</i> and <i>dwAPIHighVersion</i>.

### -param lpExtensionID

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>. If the service provider for the specified <i>dwDeviceID</i> supports provider-specific extensions, then, upon a successful negotiation, this structure is filled with the extension identifier of these extensions. This structure contains all zeros if the line provides no extensions. An application can ignore the returned parameter if it does not use extensions.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_OPERATIONUNAVAIL, LINEERR_NODEVICE.

## -remarks

Use 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> to determine the number of line devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of line devices present.

The 
<b>lineNegotiateAPIVersion</b> function is used to negotiate the API version number to use. It also retrieves the extension identifier supported by the line device, and returns zeros if no extensions are supported. If the application wants to use the extensions defined by the returned extension identifier, it must call 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateextversion">lineNegotiateExtVersion</a> to negotiate the extension version to use.

The API version number negotiated is that under which TAPI can operate. If version ranges do not overlap, the application and API or service provider versions are incompatible and an error is returned.

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineextensionid">LINEEXTENSIONID</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/Tapi/tapi-versioning">TAPI Versioning</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateextversion">lineNegotiateExtVersion</a>