---
UID: NF:tspi.TSPI_lineGetNumAddressIDs
title: TSPI_lineGetNumAddressIDs function (tspi.h)
description: The TSPI_lineGetNumAddressIDs function retrieves the number of address identifiers supported on the indicated line.
helpviewer_keywords: ["TSPI_lineGetNumAddressIDs","TSPI_lineGetNumAddressIDs function [TAPI 2.2]","_tspi_tspi_linegetnumaddressids","tspi.tspi_linegetnumaddressids","tspi/TSPI_lineGetNumAddressIDs"]
old-location: tspi\tspi_linegetnumaddressids.htm
tech.root: tapi3
ms.assetid: 53fd70eb-2694-4c8c-97cd-6ee9f2606ced
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetNumAddressIDs, TSPI_lineGetNumAddressIDs function [TAPI 2.2], _tspi_tspi_linegetnumaddressids, tspi.tspi_linegetnumaddressids, tspi/TSPI_lineGetNumAddressIDs
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
 - TSPI_lineGetNumAddressIDs
 - tspi/TSPI_lineGetNumAddressIDs
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
 - TSPI_lineGetNumAddressIDs
---

# TSPI_lineGetNumAddressIDs function


## -description

The 
<b>TSPI_lineGetNumAddressIDs</b> function retrieves the number of address identifiers supported on the indicated line.

## -parameters

### -param hdLine

The handle to the line for which the number of address identifiers is to be retrieved.

### -param lpdwNumAddressIDs

A pointer to a <b>DWORD</b>. The location is filled with the number of address identifiers supported on the indicated line. The value is one or larger.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

This function is called by TAPI in response to an application calling 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a>, 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetnumrings">lineGetNumRings</a>, or 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetnewcalls">lineGetNewCalls</a>. TAPI uses the retrieved value to determine if the specified address identifier is within the range supported by the service provider.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linegetnewcalls">lineGetNewCalls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetnumrings">lineGetNumRings</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a>