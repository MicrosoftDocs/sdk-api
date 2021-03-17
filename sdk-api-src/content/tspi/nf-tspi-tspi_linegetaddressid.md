---
UID: NF:tspi.TSPI_lineGetAddressID
title: TSPI_lineGetAddressID function (tspi.h)
description: The TSPI_lineGetAddressID function returns the address identifier associated with address in a different format on the specified line.
helpviewer_keywords: ["TSPI_lineGetAddressID","TSPI_lineGetAddressID function [TAPI 2.2]","_tspi_tspi_linegetaddressid","tspi.tspi_linegetaddressid","tspi/TSPI_lineGetAddressID"]
old-location: tspi\tspi_linegetaddressid.htm
tech.root: tapi3
ms.assetid: 8783fb72-a50c-444c-aa89-485cb0eb6739
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetAddressID, TSPI_lineGetAddressID function [TAPI 2.2], _tspi_tspi_linegetaddressid, tspi.tspi_linegetaddressid, tspi/TSPI_lineGetAddressID
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
 - TSPI_lineGetAddressID
 - tspi/TSPI_lineGetAddressID
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
 - TSPI_lineGetAddressID
---

# TSPI_lineGetAddressID function


## -description

The 
<b>TSPI_lineGetAddressID</b> function returns the address identifier associated with address in a different format on the specified line.

## -parameters

### -param hdLine

The service provider's handle to the line whose address is to be retrieved.

### -param lpdwAddressID

A pointer to a <b>DWORD</b>-sized memory location where the address identifier is returned.

### -param dwAddressMode

The address mode of the address contained in <i>lpsAddress</i>. The <i>dwAddressMode</i> parameter is allowed to have one and only one of the 
<a href="/windows/desktop/Tapi/lineaddressmode--constants">LINEADDRESSMODE_ constants</a>.

### -param lpsAddress

A pointer to a data structure holding the address assigned to the specified line device. The format of the address is determined by the <i>dwAddressMode</i> parameter. If it is LINEADDRESSMODE_DIALABLEADDR, the <i>lpsAddress</i> parameter uses the common dialable number format and is <b>NULL</b> terminated.

### -param dwSize

The size of the address contained in <i>lpsAddress</i>. The parameter <i>dwSize</i> must be set to the length of the string (plus one for the <b>NULL</b>) if LINEADDRESSMODE_DIALABLEADDR is used. If an extended LINEADDRESSMODE is used, the length should match the size of whatever is actually passed in (the DLL checks to be sure it can read the number of bytes specified from the given pointer).

## -returns

Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESS, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -remarks

This function is used to map a phone number (address) assigned to a line device back to its <i>dwAddressID</i> (in the range from 0 through the number of addresses minus one) that is returned in the line's device capabilities.

## -see-also

<a href="/windows/desktop/Tapi/lineaddressmode--constants">LINEADDRESSMODE_ Constants</a>