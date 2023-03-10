---
UID: NF:tspi.TSPI_phoneGetDevCaps
title: TSPI_phoneGetDevCaps function (tspi.h)
description: The TSPI_phoneGetDevCaps function queries a specified phone device to determine its telephony capabilities.
helpviewer_keywords: ["TSPI_phoneGetDevCaps","TSPI_phoneGetDevCaps function [TAPI 2.2]","_tspi_tspi_phonegetdevcaps","tspi.tspi_phonegetdevcaps","tspi/TSPI_phoneGetDevCaps"]
old-location: tspi\tspi_phonegetdevcaps.htm
tech.root: tapi3
ms.assetid: d929ed39-ba1d-4eae-9667-86d904ba96a8
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetDevCaps, TSPI_phoneGetDevCaps function [TAPI 2.2], _tspi_tspi_phonegetdevcaps, tspi.tspi_phonegetdevcaps, tspi/TSPI_phoneGetDevCaps
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_phoneGetDevCaps
 - tspi/TSPI_phoneGetDevCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetDevCaps
---

# TSPI_phoneGetDevCaps function


## -description

The 
<b>TSPI_phoneGetDevCaps</b> function queries a specified phone device to determine its telephony capabilities.

## -parameters

### -param dwDeviceID

The phone device to be queried.

### -param dwTSPIVersion

The negotiated TSPI version number. This value is negotiated for this device through the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion">TSPI_phoneNegotiateTSPIVersion</a> function.

### -param dwExtVersion

The negotiated extension version number. This value is negotiated for this device through the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a> function.

### -param lpPhoneCaps

A pointer to memory into which the service provider writes a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>. Upon successful completion of the request, this structure is filled with phone device capability information. Prior to calling 
<b>TSPI_phoneGetDevCaps</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_NODRIVER, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.

## -remarks

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

If <i>dwExtVersion</i> is zero, no extension information is requested. If it is nonzero, it holds a value that has already been negotiated for this device with the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a> function. The service provider fills in device- and vendor-specific extended information according to the extension version specified.

After the service provider returns from the 
<b>TSPI_phoneGetDevCaps</b> function, TAPI sets the <b>dwPhoneStates</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a> structure as follows:


``` syntax
PHONECAPS.dwPhoneStates |=
    PHONESTATE_OWNER |
    PHONESTATE_MONITORS |
    PHONESTATE_REINIT;
```


## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonecaps">PHONECAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>
