---
UID: NF:tspi.TSPI_lineGetDevCaps
title: TSPI_lineGetDevCaps function (tspi.h)
description: The TSPI_lineGetDevCaps function queries a specified line device to determine its telephony capabilities. The returned information is valid for all addresses on the line device.
helpviewer_keywords: ["TSPI_lineGetDevCaps","TSPI_lineGetDevCaps function [TAPI 2.2]","_tspi_tspi_linegetdevcaps","tspi.tspi_linegetdevcaps","tspi/TSPI_lineGetDevCaps"]
old-location: tspi\tspi_linegetdevcaps.htm
tech.root: tapi3
ms.assetid: 6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetDevCaps, TSPI_lineGetDevCaps function [TAPI 2.2], _tspi_tspi_linegetdevcaps, tspi.tspi_linegetdevcaps, tspi/TSPI_lineGetDevCaps
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
 - TSPI_lineGetDevCaps
 - tspi/TSPI_lineGetDevCaps
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
 - TSPI_lineGetDevCaps
---

# TSPI_lineGetDevCaps function


## -description

The 
<b>TSPI_lineGetDevCaps</b> function queries a specified line device to determine its telephony capabilities. The returned information is valid for all addresses on the line device.

## -parameters

### -param dwDeviceID

The line device to be queried.

### -param dwTSPIVersion

The negotiated TSPI version number. This value has already been negotiated for this device through the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a> function.

### -param dwExtVersion

The negotiated extension version number. This value has already been negotiated for this device through the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a> function. This parameter is not validated by TAPI when this function is called.

### -param lpLineDevCaps

A pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>. Upon successful completion of the request, this structure is filled with line device capabilities information.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.

## -remarks

Line device identifier numbering for a service provider is sequential from the value set by the <i>dwLineDeviceIDBase</i> parameter that is passed to the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> function.

The <i>dwExtVersion</i> formal parameter indicates the version number of the requested extension information. If it is zero, no extension information is requested. If it is nonzero, it holds a value that was negotiated for this device with the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a> function. The service provider fills in device- and vendor-specific extended information according to the extension version specified.

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

The service provider must fill in all members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetermcaps">LINETERMCAPS</a> data structure or structures embedded in the varying part of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> data structure.

After the service provider returns from the 
<b>TSPI_lineGetDevCaps</b> function, TAPI sets the <b>dwLinesStates</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure as follows:


``` syntax
LINEDEVCAPS.dwLineStates |=
    LINEDEVSTATE_OPEN |
    LINEDEVSTATE_CLOSE |
    LINEDEVSTATE_REINIT |
    LINEDEVSTATE_TRANSLATECHANGE;
```


## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetermcaps">LINETERMCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>
