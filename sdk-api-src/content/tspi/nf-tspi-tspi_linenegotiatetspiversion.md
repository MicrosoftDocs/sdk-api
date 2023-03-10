---
UID: NF:tspi.TSPI_lineNegotiateTSPIVersion
title: TSPI_lineNegotiateTSPIVersion function (tspi.h)
description: The TSPI_lineNegotiateTSPIVersion function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.
helpviewer_keywords: ["TSPI_lineNegotiateTSPIVersion","TSPI_lineNegotiateTSPIVersion function [TAPI 2.2]","_tspi_tspi_linenegotiatetspiversion","tspi.tspi_linenegotiatetspiversion","tspi/TSPI_lineNegotiateTSPIVersion"]
old-location: tspi\tspi_linenegotiatetspiversion.htm
tech.root: tapi3
ms.assetid: d92fbf18-282d-485b-9d56-22e4896ece57
ms.date: 12/05/2018
ms.keywords: TSPI_lineNegotiateTSPIVersion, TSPI_lineNegotiateTSPIVersion function [TAPI 2.2], _tspi_tspi_linenegotiatetspiversion, tspi.tspi_linenegotiatetspiversion, tspi/TSPI_lineNegotiateTSPIVersion
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
 - TSPI_lineNegotiateTSPIVersion
 - tspi/TSPI_lineNegotiateTSPIVersion
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
 - TSPI_lineNegotiateTSPIVersion
---

# TSPI_lineNegotiateTSPIVersion function


## -description

The 
<b>TSPI_lineNegotiateTSPIVersion</b> function returns the highest SPI version the service provider can operate under for this device, given the range of possible SPI versions.

## -parameters

### -param dwDeviceID

Identifies the line device for which interface version negotiation is to be performed. In addition to device identifiers within the range the service provider supports, this may be the value: 







#### INITIALIZE_NEGOTIATION

This value is used to signify that an overall interface version is to be negotiated.

### -param dwLowVersion

The lowest TSPI version number under which TAPI can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.

### -param dwHighVersion

The highest TSPI version number under which TAPI can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.

### -param lpdwTSPIVersion

A pointer to a <b>DWORD</b>. The service provider fills this location with the highest TSPI version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns LINEERR_INCOMPATIBLEAPIVERSION.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

When <i>dwDeviceID</i> is 
<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a>, this function must not return LINEERR_OPERATIONUNAVAIL, because this function (with that value) is mandatory for negotiating the overall interface version even if the service provider supports no line devices.

## -see-also

<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a>



<a href="/windows/desktop/Tapi/tspi-versioning">TSPI Versioning</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetextensionid">TSPI_lineGetExtensionID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>