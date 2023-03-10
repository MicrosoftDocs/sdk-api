---
UID: NF:tspi.TSPI_lineGetCallAddressID
title: TSPI_lineGetCallAddressID function (tspi.h)
description: The TSPI_lineGetCallAddressID function retrieves the address identifier for the indicated call.
helpviewer_keywords: ["TSPI_lineGetCallAddressID","TSPI_lineGetCallAddressID function [TAPI 2.2]","_tspi_tspi_linegetcalladdressid","tspi.tspi_linegetcalladdressid","tspi/TSPI_lineGetCallAddressID"]
old-location: tspi\tspi_linegetcalladdressid.htm
tech.root: tapi3
ms.assetid: 8dffbaa5-77fc-4653-84f9-f8e08141ee0e
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetCallAddressID, TSPI_lineGetCallAddressID function [TAPI 2.2], _tspi_tspi_linegetcalladdressid, tspi.tspi_linegetcalladdressid, tspi/TSPI_lineGetCallAddressID
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
 - TSPI_lineGetCallAddressID
 - tspi/TSPI_lineGetCallAddressID
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
 - TSPI_lineGetCallAddressID
---

# TSPI_lineGetCallAddressID function


## -description

The 
<b>TSPI_lineGetCallAddressID</b> function retrieves the address identifier for the indicated call.

## -parameters

### -param hdCall

The service provider's handle to the call whose address identifier is to be retrieved. The call state of <i>hdCall</i> can be any state.

### -param lpdwAddressID

A pointer to a <b>DWORD</b> into which the service provider writes the call's address identifier.

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -remarks

If the service provider models lines as "pools" of channel resources and does inverse multiplexing of a call over several address identifiers it should consistently choose one of these address identifiers as the primary identifier reported by this function and in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> data structure.

This function has no direct correspondence at the TAPI level. It gives TAPI sufficient information to implement the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetnewcalls">lineGetNewCalls</a> function invoked with the LINECALLSELECT_ADDRESS option.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>