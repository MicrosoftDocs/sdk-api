---
UID: NF:tspi.TSPI_phoneNegotiateTSPIVersion
title: TSPI_phoneNegotiateTSPIVersion function (tspi.h)
description: The TSPI_phoneNegotiateTSPIVersion function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.
helpviewer_keywords: ["TSPI_phoneNegotiateTSPIVersion","TSPI_phoneNegotiateTSPIVersion function [TAPI 2.2]","_tspi_tspi_phonenegotiatetspiversion","tspi.tspi_phonenegotiatetspiversion","tspi/TSPI_phoneNegotiateTSPIVersion"]
old-location: tspi\tspi_phonenegotiatetspiversion.htm
tech.root: tapi3
ms.assetid: a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc
ms.date: 12/05/2018
ms.keywords: TSPI_phoneNegotiateTSPIVersion, TSPI_phoneNegotiateTSPIVersion function [TAPI 2.2], _tspi_tspi_phonenegotiatetspiversion, tspi.tspi_phonenegotiatetspiversion, tspi/TSPI_phoneNegotiateTSPIVersion
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
 - TSPI_phoneNegotiateTSPIVersion
 - tspi/TSPI_phoneNegotiateTSPIVersion
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
 - TSPI_phoneNegotiateTSPIVersion
---

# TSPI_phoneNegotiateTSPIVersion function


## -description

The 
<b>TSPI_phoneNegotiateTSPIVersion</b> function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.

## -parameters

### -param dwDeviceID

The phone device for which interface version negotiation is to be performed. Permitted values are strictly within the range of phone devices identifiers for this service provider; the value 
<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a> is never passed to this function.

### -param dwLowVersion

The lowest TSPI version number under which TAPI can operate. The most significant <b>WORD</b> is the major version number and the least significant <b>WORD</b> is the minor version number.

### -param dwHighVersion

The highest TSPI version number under which TAPI can operate. The most significant <b>WORD</b> is the major version number and the least significant <b>WORD</b> is the minor version number.

### -param lpdwTSPIVersion

A pointer to a <b>DWORD</b>. Upon a successful return from this function the service provider fills this location with the highest TSPI version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns PHONEERR_INCOMPATIBLEAPIVERSION.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODRIVER, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

The service provider returns PHONEERR_OPERATIONUNAVAIL if the operation is not available. However, if the service provider supports any phone devices, it must also support this function and the function must not return PHONEERR_OPERATIONUNAVAIL.

TAPI calls this function early in the initialization sequence for each phone device.

Negotiation of an extension version is done through the separate procedure 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>.

The corresponding function at the TAPI level is an overloaded function that also retrieves the extension identifier, if any, supported by the service provider. At the TSPI level, retrieving the extension identifier is accomplished through a separate procedure, namely, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetextensionid">TSPI_phoneGetExtensionID</a>.

## -see-also

<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetextensionid">TSPI_phoneGetExtensionID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>