---
UID: NF:tapi.lineNegotiateExtVersion
title: lineNegotiateExtVersion function (tapi.h)
description: The lineNegotiateExtVersion function allows an application to negotiate an extension version to use with the specified line device. This operation need not be called if the application does not support extensions.
helpviewer_keywords: ["_tapi2_linenegotiateextversion","lineNegotiateExtVersion","lineNegotiateExtVersion function [TAPI 2.2]","tapi/lineNegotiateExtVersion","tapi2.linenegotiateextversion"]
old-location: tapi2\linenegotiateextversion.htm
tech.root: tapi3
ms.assetid: 89a49709-a15b-4358-984a-fd836d8e237b
ms.date: 12/05/2018
ms.keywords: _tapi2_linenegotiateextversion, lineNegotiateExtVersion, lineNegotiateExtVersion function [TAPI 2.2], tapi/lineNegotiateExtVersion, tapi2.linenegotiateextversion
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
 - lineNegotiateExtVersion
 - tapi/lineNegotiateExtVersion
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
 - lineNegotiateExtVersion
---

# lineNegotiateExtVersion function


## -description

The 
<b>lineNegotiateExtVersion</b> function allows an application to negotiate an extension version to use with the specified line device. This operation need not be called if the application does not support extensions.

## -parameters

### -param hLineApp

Handle to the application's registration with TAPI.

### -param dwDeviceID

Identifier of the line device to be queried.

### -param dwAPIVersion

TAPI version number that was negotiated for the specified line device using 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>.

### -param dwExtLowVersion

Earliest extension version of the extension identifier returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.

### -param dwExtHighVersion

Latest extension version of the extension identifier returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.

### -param lpdwExtVersion

Pointer to a variable that contains the extension version number that was negotiated. If negotiation succeeds, this number is in the range between <i>dwExtLowVersion</i> and <i>dwExtHighVersion</i>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NODRIVER, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NODEVICE, LINEERR_OPERATIONUNAVAIL.

## -remarks

Use 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> to determine the number of line devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of line devices present.

The 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a> function negotiates the API version number to use. It also retrieves the extension identifier supported by the line device, which is zeros if no extensions are provided. Version numbers should be incremented by one for each release. Leaving gaps in release version numbering can cause unexpected results.

If the application wants to use the extensions defined by the returned extension identifier, it must call 
<b>lineNegotiateExtVersion</b> to negotiate the extension version to use.

The extension version number negotiated is that under which the application and service provider must both operate. If version ranges do not overlap, the application and service provider versions are incompatible and an error is returned.

## -see-also

<a href="/windows/desktop/Tapi/extended-telephony-services-reference">Extended Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>