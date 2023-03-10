---
UID: NF:tapi.lineGetNumRings
title: lineGetNumRings function (tapi.h)
description: The lineGetNumRings function determines the number of rings an incoming call on the given address should ring prior to answering the call.
helpviewer_keywords: ["_tapi2_linegetnumrings","lineGetNumRings","lineGetNumRings function [TAPI 2.2]","tapi/lineGetNumRings","tapi2.linegetnumrings"]
old-location: tapi2\linegetnumrings.htm
tech.root: tapi3
ms.assetid: 7aee6396-6045-4e7b-9df9-3729159ea4b2
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetnumrings, lineGetNumRings, lineGetNumRings function [TAPI 2.2], tapi/lineGetNumRings, tapi2.linegetnumrings
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGetNumRings
 - tapi/lineGetNumRings
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
 - lineGetNumRings
---

# lineGetNumRings function


## -description

The 
<b>lineGetNumRings</b> function determines the number of rings an incoming call on the given address should ring prior to answering the call.

## -parameters

### -param hLine

Handle to the open line device.

### -param dwAddressID

Address on the line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.

### -param lpdwNumRings

Number of rings that is the minimum of all current 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a> requests.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

## -remarks

The 
<b>lineGetNumRings</b> and 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a> functions, when used in combination, provide a mechanism to support the implementation of toll-saver features across multiple independent applications.

An application that receives a handle for a call in the <i>offering</i> state and a 
<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a> <i>ringing</i> message should wait a number of rings equal to the number returned by 
<b>lineGetNumRings</b> before answering the call in order to honor the toll-saver settings across all applications. The 
<b>lineGetNumRings</b> function returns the minimum of all applications' number of rings specified by 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a>. Because this number can vary dynamically, an application should invoke 
<b>lineGetNumRings</b> each time it has the option to answer a call. If no application has called 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a>, the number of rings returned is 0xFFFFFFFF. A separate LINE_LINEDEVSTATE <i>ringing</i> message is sent to the application for each ring cycle.

If call classification is performed by TAPI of answering all calls of unknown media mode and filtering the media stream, TAPI honors this number as well.

<div class="alert"><b>Note</b>  This operation is purely informational and does not in itself affect the state of any calls on the line device.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-linedevstate">LINE_LINEDEVSTATE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetnumrings">lineSetNumRings</a>