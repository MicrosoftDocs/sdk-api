---
UID: NS:tapi.lineaddressstatus_tag
title: LINEADDRESSSTATUS (tapi.h)
description: The LINEADDRESSSTATUS structure describes the current status of an address. The lineGetAddressStatus function and the TSPI_lineGetAddressStatus function return the LINEADDRESSSTATUS structure.
helpviewer_keywords: ["*LPLINEADDRESSSTATUS","LINEADDRESSSTATUS","LINEADDRESSSTATUS structure [TAPI 2.2]","LPLINEADDRESSSTATUS","LPLINEADDRESSSTATUS structure pointer [TAPI 2.2]","_tapi2_lineaddressstatus_str","tapi/LINEADDRESSSTATUS","tapi/LPLINEADDRESSSTATUS","tapi2.lineaddressstatus_str"]
old-location: tapi2\lineaddressstatus_str.htm
tech.root: tapi3
ms.assetid: 795aa97d-76a9-4041-b9f6-345644561043
ms.date: 12/05/2018
ms.keywords: '*LPLINEADDRESSSTATUS, LINEADDRESSSTATUS, LINEADDRESSSTATUS structure [TAPI 2.2], LPLINEADDRESSSTATUS, LPLINEADDRESSSTATUS structure pointer [TAPI 2.2], _tapi2_lineaddressstatus_str, tapi/LINEADDRESSSTATUS, tapi/LPLINEADDRESSSTATUS, tapi2.lineaddressstatus_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEADDRESSSTATUS, *LPLINEADDRESSSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineaddressstatus_tag
 - tapi/lineaddressstatus_tag
 - LPLINEADDRESSSTATUS
 - tapi/LPLINEADDRESSSTATUS
 - LINEADDRESSSTATUS
 - tapi/LINEADDRESSSTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEADDRESSSTATUS
---

# LINEADDRESSSTATUS structure


## -description

The 
<b>LINEADDRESSSTATUS</b> structure describes the current status of an address. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddressstatus">lineGetAddressStatus</a> function and the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddressstatus">TSPI_lineGetAddressStatus</a> function return the 
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
<a href="/windows/desktop/Tapi/lineaddrfeature--constants">LINEADDRFEATURE_ constants</a>.

### -field dwNumRingsNoAnswer

Number of rings set for this address before an unanswered call is considered as no answer.

### -field dwForwardNumEntries

Number of entries in the array referred to by <b>dwForwardSize</b> and <b>dwForwardOffset</b>.

### -field dwForwardSize

Size of the forwarding information array, in bytes.

### -field dwForwardOffset

Offset from the beginning of the structure to the variably sized field that describes the address's forwarding information. This information is an array of <b>dwForwardNumEntries</b> elements, of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a>. The offsets of the addresses in the array are relative to the beginning of the 
<b>LINEADDRESSSTATUS</b> structure. The offsets <b>dwCallerAddressOffset</b> and <b>dwDestAddressOffset</b> in the variably sized field of type 
<b>LINEFORWARD</b> pointed to by <i>dwForwardOffset</i> are relative to the beginning of the 
<b>LINEADDRESSSTATUS</b> data structure (the "root" container). The size of the array is specified by <b>dwForwardSize</b>.

### -field dwTerminalModesSize

Size of the terminal modes array, in bytes.

### -field dwTerminalModesOffset

Offset from the beginning of the structure to the variably sized device field containing an array with <b>DWORD</b>-sized entries, that use one or more of the 
<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ constants</a>. This array is indexed by terminal identifiers, in the range from zero to one less than <b>dwNumTerminals</b>. Each entry in the array specifies the current terminal modes for the corresponding terminal set with the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a> function for this address. The size of the array is specified by <b>dwTerminalModesSize</b>.

### -field dwDevSpecificSize

Size of the device-specific field, in bytes.

### -field dwDevSpecificOffset

Offset from the beginning of this structure to the variably sized device-specific field. The size of the field is specified by <b>dwDevSpecificSize</b>.

## -remarks

Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

This data structure is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddressstatus">lineGetAddressStatus</a> function. When items in this data structure change as a consequence of activities on the address, a 
<a href="/windows/desktop/Tapi/line-addressstate">LINE_ADDRESSSTATE</a> message is sent to the application. A parameter to this message is the address state, one of the 
<a href="/windows/desktop/Tapi/lineaddressstate--constants">LINEADDRESSSTATE_ constants</a>, which indicates that the status item in this record changed.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineforward">LINEFORWARD</a>



<a href="/windows/desktop/Tapi/line-addressstate">LINE_ADDRESSSTATE</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetaddressstatus">TSPI_lineGetAddressStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddressstatus">lineGetAddressStatus</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a>