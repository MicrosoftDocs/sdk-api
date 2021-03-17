---
UID: NF:tspi.TSPI_lineGetAddressStatus
title: TSPI_lineGetAddressStatus function (tspi.h)
description: The TSPI_lineGetAddressStatus function queries the specified address for its current status.
helpviewer_keywords: ["TSPI_lineGetAddressStatus","TSPI_lineGetAddressStatus function [TAPI 2.2]","_tspi_tspi_linegetaddressstatus","tspi.tspi_linegetaddressstatus","tspi/TSPI_lineGetAddressStatus"]
old-location: tspi\tspi_linegetaddressstatus.htm
tech.root: tapi3
ms.assetid: e3afd959-a0cb-4f0a-a700-d50cf7a4c386
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetAddressStatus, TSPI_lineGetAddressStatus function [TAPI 2.2], _tspi_tspi_linegetaddressstatus, tspi.tspi_linegetaddressstatus, tspi/TSPI_lineGetAddressStatus
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
 - TSPI_lineGetAddressStatus
 - tspi/TSPI_lineGetAddressStatus
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
 - TSPI_lineGetAddressStatus
---

# TSPI_lineGetAddressStatus function


## -description

The 
<b>TSPI_lineGetAddressStatus</b> function queries the specified address for its current status.

## -parameters

### -param hdLine

The service provider's handle to the line containing the address to be queried.

### -param dwAddressID

An address on the given open line device. This is the address to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. This parameter is not validated by TAPI when this function is called.

### -param lpAddressStatus

A pointer to a variably sized data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineaddressstatus">LINEADDRESSSTATUS</a>