---
UID: NF:tspi.TSPI_lineGetAddressCaps
title: TSPI_lineGetAddressCaps function (tspi.h)
description: The TSPI_lineGetAddressCaps function queries the specified address on the specified line device to determine its telephony capabilities.
helpviewer_keywords: ["TSPI_lineGetAddressCaps","TSPI_lineGetAddressCaps function [TAPI 2.2]","_tspi_tspi_linegetaddresscaps","tspi.tspi_linegetaddresscaps","tspi/TSPI_lineGetAddressCaps"]
old-location: tspi\tspi_linegetaddresscaps.htm
tech.root: tapi3
ms.assetid: b8d52a94-2666-4f92-80e0-c9a1e04d1e79
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetAddressCaps, TSPI_lineGetAddressCaps function [TAPI 2.2], _tspi_tspi_linegetaddresscaps, tspi.tspi_linegetaddresscaps, tspi/TSPI_lineGetAddressCaps
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
 - TSPI_lineGetAddressCaps
 - tspi/TSPI_lineGetAddressCaps
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
 - TSPI_lineGetAddressCaps
---

# TSPI_lineGetAddressCaps function


## -description

The 
<b>TSPI_lineGetAddressCaps</b> function queries the specified address on the specified line device to determine its telephony capabilities.

## -parameters

### -param dwDeviceID

The line device containing the address to be queried.

### -param dwAddressID

The address on the given line device whose capabilities are to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. This parameter is not validated by TAPI when this function is called.

### -param dwTSPIVersion

The version number of the Telephony SPI to be used. The high-order word contains the major version number; the low-order word contains the minor version number.

### -param dwExtVersion

The version number of the service-provider specific extensions to be used. This number is zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; the low-order word contain the minor version number. This parameter is not validated by TAPI when this function is called.

### -param lpAddressCaps

A pointer to a variably sized structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>. Upon successful completion of the request, this structure is filled with address capabilities information.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NOMEM, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL.

## -remarks

The line device identifiers supported by a particular driver are numbered sequentially starting with the value of <i>dwLineDeviceIDBase</i> that is passed into the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a> function.

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

After the service provider returns from the 
<b>TSPI_lineGetAddressCaps</b> function, TAPI sets the <b>dwCallInfoStates</b> and <b>dwCallStates</b> members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> structure as follows:


``` syntax
LINEADDRESSCAPS.dwCallInfoStates |=
    LINECALLINFOSTATE_NUMOWNERINCR |
    LINECALLINFOSTATE_NUMOWNERDECR |
    LINECALLINFOSTATE_NUMMONITORS;

LINEADDRESSCAPS.dwCallStates |= LINECALLSTATE_UNKNOWN;
```


## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_providerinit">TSPI_providerInit</a>
