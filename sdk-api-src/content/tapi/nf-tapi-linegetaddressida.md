---
UID: NF:tapi.lineGetAddressIDA
title: lineGetAddressIDA function
author: windows-sdk-content
description: The lineGetAddressID function returns the address identifier associated with an address in a different format on the specified line.
old-location: tapi2\linegetaddressid.htm
old-project: Tapi
ms.assetid: f714068c-8cdc-4098-b1f6-f2cfd62a83c4
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linegetaddressid, lineGetAddressID, lineGetAddressID function [TAPI 2.2], lineGetAddressIDA, lineGetAddressIDW, tapi/lineGetAddressID, tapi/lineGetAddressIDA, tapi/lineGetAddressIDW, tapi2.linegetaddressid"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineGetAddressID
-	lineGetAddressIDA
-	lineGetAddressIDW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetAddressIDA function


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
<a href="https://msdn.microsoft.com/f0f132a0-2e8e-478f-909b-c100aa360daa">LINEADDRESSMODE_ Constants</a>. You must specify LINEADDRESSMODE_DIALABLEADDR.


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
<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a> function allows the application to make a call by specifying a line handle and an address on the line. The address can be specified as a <i>dwAddressID</i>, as a phone number, or as a device-specific name or identifier. Using a phone number can be practical in environments where a single line is assigned multiple addresses.

<div class="alert"><b>Note</b>  LINEADDRESSMODE_ADDRESSID may not be used with 
<b>lineGetAddressID</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/a7dc9cdc-3cc3-4b6a-98c8-e141402c781e">lineMakeCall</a>
 

 

