---
UID: NF:tapi.lineGetAddressIDW
title: lineGetAddressIDW function (tapi.h)
description: The lineGetAddressIDW (Unicode) function (tapi.h) returns the address identifier associated with an address in a different format on the specified line.
helpviewer_keywords: ["_tapi2_linegetaddressid", "lineGetAddressID", "lineGetAddressID function [TAPI 2.2]", "lineGetAddressIDW", "tapi/lineGetAddressID", "tapi/lineGetAddressIDW", "tapi2.linegetaddressid"]
old-location: tapi2\linegetaddressid.htm
tech.root: tapi3
ms.assetid: f714068c-8cdc-4098-b1f6-f2cfd62a83c4
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetaddressid, lineGetAddressID, lineGetAddressID function [TAPI 2.2], lineGetAddressIDA, lineGetAddressIDW, tapi/lineGetAddressID, tapi/lineGetAddressIDA, tapi/lineGetAddressIDW, tapi2.linegetaddressid
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAddressIDW (Unicode) and lineGetAddressIDA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGetAddressIDW
 - tapi/lineGetAddressIDW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetAddressID
 - lineGetAddressIDA
 - lineGetAddressIDW
---

# lineGetAddressIDW function


## -description

The 
<b>lineGetAddressID</b> function returns the address identifier associated with an address in a different format on the specified line.

## -parameters

### -param hLine

Handle to the open line device.

### -param lpdwAddressID

Pointer to a <b>DWORD</b>-sized memory location where the address identifier is returned. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param dwAddressMode

Address mode of the address contained in <i>lpsAddress</i>. This parameter uses one and only one of the 
<a href="/windows/desktop/Tapi/lineaddressmode--constants">LINEADDRESSMODE_ Constants</a>. You must specify LINEADDRESSMODE_DIALABLEADDR.

### -param lpsAddress

Pointer to a data structure holding the address assigned to the specified line device. The format of the address is determined by <i>dwAddressMode</i>. Because the only valid value is LINEADDRESSMODE_DIALABLEADDR, <i>lpsAddress</i> uses the common dialable number format and is null-terminated.

### -param dwSize

Size, in bytes, of the address contained in <i>lpsAddress</i>. The size of the string must include the null terminator.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSMODE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALADDRESS, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

The 
<b>lineGetAddressID</b> function is used to map a phone number (address) assigned to a line device back to its <i>dwAddressID</i> in the range zero to the number of addresses minus one returned in the line's device capabilities. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a> function allows the application to make a call by specifying a line handle and an address on the line. The address can be specified as a <i>dwAddressID</i>, as a phone number, or as a device-specific name or identifier. Using a phone number can be practical in environments where a single line is assigned multiple addresses.

<div class="alert"><b>Note</b>  LINEADDRESSMODE_ADDRESSID may not be used with 
<b>lineGetAddressID</b>.</div>
<div> </div>




> [!NOTE]
> The tapi.h header defines lineGetAddressID as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linemakecall">lineMakeCall</a>
