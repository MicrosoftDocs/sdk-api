---
UID: NF:tspi.TSPI_lineNegotiateExtVersion
title: TSPI_lineNegotiateExtVersion function (tspi.h)
description: The TSPI_lineNegotiateExtVersion function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.
helpviewer_keywords: ["TSPI_lineNegotiateExtVersion","TSPI_lineNegotiateExtVersion function [TAPI 2.2]","_tspi_tspi_linenegotiateextversion","tspi.tspi_linenegotiateextversion","tspi/TSPI_lineNegotiateExtVersion"]
old-location: tspi\tspi_linenegotiateextversion.htm
tech.root: tapi3
ms.assetid: cd7cc421-3efb-4fe1-858c-4d894f4d9377
ms.date: 12/05/2018
ms.keywords: TSPI_lineNegotiateExtVersion, TSPI_lineNegotiateExtVersion function [TAPI 2.2], _tspi_tspi_linenegotiateextversion, tspi.tspi_linenegotiateextversion, tspi/TSPI_lineNegotiateExtVersion
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
 - TSPI_lineNegotiateExtVersion
 - tspi/TSPI_lineNegotiateExtVersion
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
 - TSPI_lineNegotiateExtVersion
---

# TSPI_lineNegotiateExtVersion function


## -description

The 
<b>TSPI_lineNegotiateExtVersion</b> function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.

## -parameters

### -param dwDeviceID

Identifies the line device for which interface version negotiation is to be performed. The value 
<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a> may not be used for this function.

### -param dwTSPIVersion

An interface version number that has already been negotiated for this device using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.

### -param dwLowVersion

The lowest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. TAPI does not validate this parameter when this function is called.

### -param dwHighVersion

The highest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. TAPI does not validate this parameter when this function is called.

### -param lpdwExtVersion

A pointer to a <b>DWORD</b>. Upon a successful return from this function, the service provider fills this location with the highest extension version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns LINEERR_INCOMPATIBLEEXTVERSION.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.

## -remarks

This function can be called before or after the device is opened by TAPI. If the device is currently open and has an extension version selected, the function gives that version number if it is within the requested range. If the selected version number is outside the requested range, the function returns LINEERR_INCOMPATIBLEEXTVERSION.

## -see-also

<a href="/windows/desktop/Tapi/initialize-negotiation">INITIALIZE_NEGOTIATION</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>