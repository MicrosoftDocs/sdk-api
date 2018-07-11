---
UID: NS:tapi.lineaddressstatus_tag
title: lineaddressstatus_tag
author: windows-sdk-content
description: The LINEADDRESSSTATUS structure describes the current status of an address. The lineGetAddressStatus function and the TSPI_lineGetAddressStatus function return the LINEADDRESSSTATUS structure.
old-location: tapi2\lineaddressstatus_str.htm
old-project: tapi
ms.assetid: 795aa97d-76a9-4041-b9f6-345644561043
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: "*LPLINEADDRESSSTATUS, LINEADDRESSSTATUS, LINEADDRESSSTATUS structure [TAPI 2.2], LPLINEADDRESSSTATUS, LPLINEADDRESSSTATUS structure pointer [TAPI 2.2], _tapi2_lineaddressstatus_str, lineaddressstatus_tag, tapi/LINEADDRESSSTATUS, tapi/LPLINEADDRESSSTATUS, tapi2.lineaddressstatus_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
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
tech.root: 
req.typenames: LINEADDRESSSTATUS, *LPLINEADDRESSSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEADDRESSSTATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineaddressstatus_tag structure


## -description


The 
<b>LINEADDRESSSTATUS</b> structure describes the current status of an address. The 
<a href="https://msdn.microsoft.com/8d747aa5-05cc-4426-9d46-24bce6b4af26">lineGetAddressStatus</a> function and the 
<a href="https://msdn.microsoft.com/e3afd959-a0cb-4f0a-a700-d50cf7a4c386">TSPI_lineGetAddressStatus</a> function return the 
<b>LINEADDRESSSTATUS</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumInUse

Number of stations that are currently using the address.


### -field dwNumActiveCalls

Number of calls on the address that are in call states other than <i>idle</i>, <i>onhold</i>, <i>onholdpendingtransfer</i>, and <i>onholdpendingconference</i>.


### -field dwNumOnHoldCalls

Number of calls on the address in the <i>onhold</i> state.


### -field dwNumOnHoldPendCalls

Number of calls on the address in the <i>onholdpendingtransfer</i> or <i>onholdpendingconference</i> state.


### -field dwAddressFeatures

Address-related functions that can be invoked on the address in its current state. This member uses one or more of the 
<a href="https://msdn.microsoft.com/dedeee7b-578b-4b19-8b99-5cd23779d661">LINEADDRFEATURE_ constants</a>.


### -field dwNumRingsNoAnswer

Number of rings set for this address before an unanswered call is considered as no answer.


### -field dwForwardNumEntries

Number of entries in the array referred to by <b>dwForwardSize</b> and <b>dwForwardOffset</b>.


### -field dwForwardSize

Size of the forwarding information array, in bytes.


### -field dwForwardOffset

Offset from the beginning of the structure to the variably sized field that describes the address's forwarding information. This information is an array of <b>dwForwardNumEntries</b> elements, of type 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>. The offsets of the addresses in the array are relative to the beginning of the 
<b>LINEADDRESSSTATUS</b> structure. The offsets <b>dwCallerAddressOffset</b> and <b>dwDestAddressOffset</b> in the variably sized field of type 
<b>LINEFORWARD</b> pointed to by <i>dwForwardOffset</i> are relative to the beginning of the 
<b>LINEADDRESSSTATUS</b> data structure (the "root" container). The size of the array is specified by <b>dwForwardSize</b>.


### -field dwTerminalModesSize

Size of the terminal modes array, in bytes.


### -field dwTerminalModesOffset

Offset from the beginning of the structure to the variably sized device field containing an array with <b>DWORD</b>-sized entries, that use one or more of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ constants</a>. This array is indexed by terminal identifiers, in the range from zero to one less than <b>dwNumTerminals</b>. Each entry in the array specifies the current terminal modes for the corresponding terminal set with the 
<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a> function for this address. The size of the array is specified by <b>dwTerminalModesSize</b>.


### -field dwDevSpecificSize

Size of the device-specific field, in bytes.


### -field dwDevSpecificOffset

Offset from the beginning of this structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

This data structure is returned by the 
<a href="https://msdn.microsoft.com/8d747aa5-05cc-4426-9d46-24bce6b4af26">lineGetAddressStatus</a> function. When items in this data structure change as a consequence of activities on the address, a 
<a href="https://msdn.microsoft.com/af211fa1-79f8-49ac-a1d8-b62981f50519">LINE_ADDRESSSTATE</a> message is sent to the application. A parameter to this message is the address state, one of the 
<a href="https://msdn.microsoft.com/f06140d0-f41a-4228-93c5-21d609af5473">LINEADDRESSSTATE_ constants</a>, which indicates that the status item in this record changed.




## -see-also




<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>



<a href="https://msdn.microsoft.com/af211fa1-79f8-49ac-a1d8-b62981f50519">LINE_ADDRESSSTATE</a>



<a href="https://msdn.microsoft.com/e3afd959-a0cb-4f0a-a700-d50cf7a4c386">TSPI_lineGetAddressStatus</a>



<a href="https://msdn.microsoft.com/8d747aa5-05cc-4426-9d46-24bce6b4af26">lineGetAddressStatus</a>



<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a>
 

 

