---
UID: NF:tapi.lineSetNumRings
title: lineSetNumRings function (tapi.h)
author: windows-sdk-content
description: The lineSetNumRings function sets the number of rings that must occur before an incoming call is answered.
old-location: tapi2\linesetnumrings.htm
tech.root: Tapi
ms.assetid: d600fd39-4e58-421c-81bf-1555f5745f5e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_tapi2_linesetnumrings, lineSetNumRings, lineSetNumRings function [TAPI 2.2], tapi/lineSetNumRings, tapi2.linesetnumrings"
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSetNumRings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSetNumRings function


## -description


The 
<b>lineSetNumRings</b> function sets the number of rings that must occur before an incoming call is answered. This function can be used to implement a toll-saver-style function. It allows multiple independent applications to each register the number of rings. The function 
<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a> returns the minimum number of rings requested. It can be used by the application that answers incoming calls to determine the number of rings it should wait before answering the call.


## -parameters




### -param hLine

Handle to the open line device.


### -param dwAddressID

Address on the line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param dwNumRings

Number of rings before a call should be answered in order to honor the toll-saver requests from all applications.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALADDRESSID, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



The 
<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a> and 
<b>lineSetNumRings</b> functions, when used in combination, provide a mechanism to support the implementation of toll-saver features across multiple independent applications. If no application ever calls 
<b>lineSetNumRings</b>, 
<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a> returns 0xFFFFFFFF.

An application that is the owner of a call in the <i>offering</i> state and that received a 
<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>  <i>ringing</i> message should wait a number of rings equal to the number returned by 
<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a> before answering the call in order to honor the toll-saver settings across all applications. A separate LINE_LINEDEVSTATE <i>ringing</i> message is sent to the application for each ring cycle, so the application should count these messages. If this call disconnects before being answered, and another call comes in shortly thereafter, the 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> message should allow the application to determine that ringing is related to the second call.

If call classification is performed by TAPI by means of answering incoming calls of unknown media type and filtering the media stream, TAPI honors this number as well.

<div class="alert"><b>Note</b>  This operation is purely informational and does not affect the state of any calls on the line device.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a>
 

 

