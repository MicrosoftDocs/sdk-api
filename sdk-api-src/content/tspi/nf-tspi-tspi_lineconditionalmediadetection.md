---
UID: NF:tspi.TSPI_lineConditionalMediaDetection
title: TSPI_lineConditionalMediaDetection function (tspi.h)
description: The TSPI_lineConditionalMediaDetection function is invoked by TAPI whenever a client application uses LINEMAPPER as the dwDeviceID in a lineOpen function call.
helpviewer_keywords: ["TSPI_lineConditionalMediaDetection","TSPI_lineConditionalMediaDetection function [TAPI 2.2]","_tspi_tspi_lineconditionalmediadetection","tspi.tspi_lineconditionalmediadetection","tspi/TSPI_lineConditionalMediaDetection"]
old-location: tspi\tspi_lineconditionalmediadetection.htm
tech.root: tapi3
ms.assetid: 8fa3f9ab-1749-43c8-b2a5-c481b1f94177
ms.date: 12/05/2018
ms.keywords: TSPI_lineConditionalMediaDetection, TSPI_lineConditionalMediaDetection function [TAPI 2.2], _tspi_tspi_lineconditionalmediadetection, tspi.tspi_lineconditionalmediadetection, tspi/TSPI_lineConditionalMediaDetection
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
 - TSPI_lineConditionalMediaDetection
 - tspi/TSPI_lineConditionalMediaDetection
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
 - TSPI_lineConditionalMediaDetection
---

# TSPI_lineConditionalMediaDetection function


## -description

The 
<b>TSPI_lineConditionalMediaDetection</b> function is invoked by TAPI whenever a client application uses LINEMAPPER as the <i>dwDeviceID</i> in a 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function call to request that lines be scanned to find one that supports the desired media types and call parameters. TAPI scans based on the union of the desired media type and the other media types currently being monitored on the line, to give the service provider the opportunity to indicate if it cannot simultaneously monitor for all of the requested media types. If the service provider can monitor for the indicated set of media types and support the capabilities indicated in <i>lpCallParams</i>, it replies with a success indication. It leaves the active media monitoring modes for the line unchanged.

## -parameters

### -param hdLine

The service provider's handle to the line on which media monitoring and parameter capabilities are to be set.

### -param dwMediaModes

The media type(s) currently of interest to the calling application. This parameter uses one of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>.

### -param lpCallParams

A pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>. It describes the call parameters that the line device should be able to provide. The only relevant fields of <i>lpCallParams</i> for the purposes of this test are the following: 




<b>dwBearerMode</b>

<b>dwMinRate</b>

<b>dwMaxRate</b>

<b>dwMediaMode</b>

<b>dwCallParamFlags</b>

<b>dwAddressMode</b>

If <b>dwAddressMode</b> is LINEADDRESSMODE_ADDRESSID, any address on the line is acceptable. If <b>dwAddressMode</b> is LINEADDRESSMODE_DIALABLEADDR, indicating that a specific originating address (phone number) is searched for, or if it is a provider-specific extension, then <b>dwOrigAddressSize/Offset</b> and the portion of the variable part they refer to are also relevant. If <b>dwAddressMode</b> is a provider-specific extension, additional information can be contained in the <b>dwDeviceSpecific</b> variably sized field. All other fields are irrelevant to the function.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_INVALMEDIAMODE, LINEERR_OPERATIONUNAVAIL.

## -remarks

A TAPI 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> function that specifies a device identifier of LINEMAPPER typically results in calling this procedure for multiple line devices to hunt for a suitable line, possibly also opening as-yet unopened lines. A success result indicates that the line is suitable for the calling application's requirements.

<div class="alert"><b>Note</b>  The media monitoring modes demanded at the TSPI level are the union of monitoring modes demanded by multiple applications at the TAPI level. As a consequence, it is most common for multiple media type flags to be set simultaneously at this level. The service provider must test to determine if it can support at least the specified set, regardless of what modes are currently in effect. TAPI ensures that the <i>dwMediaModes</i> parameter has at least one bit set and that no reserved bits are set. It is the service provider's responsibility to do any further validity checks on the media types, such as checking whether any media types are supported by the service provider.</div>
<div> </div>
The 
<b>TSPI_lineConditionalMediaDetection</b> function checks the bits set in the <b>dwCallParamFlags</b> member of the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a> structure and handles the following cases:

The 
<b>TSPI_lineConditionalMediaDetection</b> function returns success if passing the same bit values to the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> function would also return success.

If the SECURE, ORIGOFFHOOK, and DESTOFFHOOK bits are set and the <i>dwAddressMode</i> parameter is LINEADDRESSMODE_ADDRESSID, the function returns success if it can succeed on one or more addresses on the line.

If the SECURE, ORIGOFFHOOK, and DESTOFFHOOK bits are set and the <i>dwAddressMode</i> parameter is LINEADDRESSMODE_DIALABLEADDR, the function returns success if it can succeed on the address identified by the <i>dwOrigAddress</i> parameter.

The service provider returns an error (for example, LINEERR_RESOURCEUNAVAIL) if, at the time this function is called, it is impossible to place a new call on the specified line device (if it would return LINEERR_CALLUNAVAIL or LINEERR_RESOURCEUNAVAIL should 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a> be invoked immediately after opening the line).

There is no directly corresponding function at the TAPI level. This procedure corresponds to the test implied for each individual line by the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> procedure when it is called with the device identifier LINEMAPPER.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallparams">LINECALLPARAMS</a>



<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linemakecall">TSPI_lineMakeCall</a>