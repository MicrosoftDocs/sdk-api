---
UID: NF:tspi.TSPI_lineOpen
title: TSPI_lineOpen function (tspi.h)
description: The TSPI_lineOpen function opens the line device whose device identifier is given, returning the service provider's handle for the device.
helpviewer_keywords: ["TSPI_lineOpen","TSPI_lineOpen function [TAPI 2.2]","_tspi_tspi_lineopen","tspi.tspi_lineopen","tspi/TSPI_lineOpen"]
old-location: tspi\tspi_lineopen.htm
tech.root: tapi3
ms.assetid: 97cde843-65bc-46ae-a6ae-724f2c9c5217
ms.date: 12/05/2018
ms.keywords: TSPI_lineOpen, TSPI_lineOpen function [TAPI 2.2], _tspi_tspi_lineopen, tspi.tspi_lineopen, tspi/TSPI_lineOpen
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
 - TSPI_lineOpen
 - tspi/TSPI_lineOpen
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
 - TSPI_lineOpen
---

# TSPI_lineOpen function


## -description

The 
<b>TSPI_lineOpen</b> function opens the line device whose device identifier is given, returning the service provider's handle for the device. The service provider must retain the TAPI handle for the device for use in subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> callback procedure.

## -parameters

### -param dwDeviceID

Identifies the line device to be opened.

### -param htLine

The TAPI handle for the line device to be used in subsequent calls to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> callback procedure to identify the device.

### -param lphdLine

A pointer to an 
<a href="/windows/desktop/Tapi/hdrvline">HDRVLINE</a> where the service provider fills in its handle for the line device.

### -param dwTSPIVersion

The TSPI version.

### -param lpfnEventProc

A pointer to the 
<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a> callback procedure supplied by TAPI that the service provider calls to report subsequent events on the line.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_ALLOCATED, LINEERR_OPERATIONUNAVAIL, LINEERR_NODRIVER, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider should reserve any non-sharable resources that are required to manage the line. However, any actions that can be postponed to 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> should be. It is a design assumption in TAPI that 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> is an "inexpensive" operation. For example, if the line is opened in monitor mode only, it should not be necessary for a COMM-port-based service provider to open the COMM port.

This procedure does not correspond directly to any procedure at the TAPI level, at which the functions of enabling device-specific extensions, selecting line characteristics, and setting media type detection are included in the functionality defined by 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>. At the TSPI level, these additional capabilities are separated out into 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection">TSPI_lineSetDefaultMediaDetection</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconditionalmediadetection">TSPI_lineConditionalMediaDetection</a>.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-lineevent">LINEEVENT</a>



<a href="/previous-versions/windows/desktop/legacy/ms725220(v=vs.85)">LINE_CLOSE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclose">TSPI_lineClose</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconditionalmediadetection">TSPI_lineConditionalMediaDetection</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiatetspiversion">TSPI_lineNegotiateTSPIVersion</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection">TSPI_lineSetDefaultMediaDetection</a>