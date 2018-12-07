---
UID: NF:tapi.lineGetNumRings
title: lineGetNumRings function
author: windows-sdk-content
description: The lineGetNumRings function determines the number of rings an incoming call on the given address should ring prior to answering the call.
old-location: tapi2\linegetnumrings.htm
tech.root: tapi
ms.assetid: 7aee6396-6045-4e7b-9df9-3729159ea4b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_tapi2_linegetnumrings, lineGetNumRings, lineGetNumRings function [TAPI 2.2], tapi/lineGetNumRings, tapi2.linegetnumrings"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - lineGetNumRings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a> requests.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.




## -remarks



The 
<b>lineGetNumRings</b> and 
<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a> functions, when used in combination, provide a mechanism to support the implementation of toll-saver features across multiple independent applications.

An application that receives a handle for a call in the <i>offering</i> state and a 
<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a> <i>ringing</i> message should wait a number of rings equal to the number returned by 
<b>lineGetNumRings</b> before answering the call in order to honor the toll-saver settings across all applications. The 
<b>lineGetNumRings</b> function returns the minimum of all applications' number of rings specified by 
<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a>. Because this number can vary dynamically, an application should invoke 
<b>lineGetNumRings</b> each time it has the option to answer a call. If no application has called 
<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a>, the number of rings returned is 0xFFFFFFFF. A separate LINE_LINEDEVSTATE <i>ringing</i> message is sent to the application for each ring cycle.

If call classification is performed by TAPI of answering all calls of unknown media mode and filtering the media stream, TAPI honors this number as well.

<div class="alert"><b>Note</b>  This operation is purely informational and does not in itself affect the state of any calls on the line device.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/15f616de-db47-4577-9a47-94f9292253dd">LINE_LINEDEVSTATE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a>
 

 

