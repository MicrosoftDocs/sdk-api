---
UID: NF:tapi.lineGetLineDevStatusW
title: lineGetLineDevStatusW function
author: windows-driver-content
description: The lineGetLineDevStatus function enables an application to query the specified open line device for its current status.
old-location: tapi2\linegetlinedevstatus.htm
old-project: Tapi
ms.assetid: 9c0fa2ba-1157-43d2-af56-aa4e0c28bd05
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "_tapi2_linegetlinedevstatus, lineGetLineDevStatus, lineGetLineDevStatus function [TAPI 2.2], lineGetLineDevStatusA, lineGetLineDevStatusW, tapi/lineGetLineDevStatus, tapi/lineGetLineDevStatusA, tapi/lineGetLineDevStatusW, tapi2.linegetlinedevstatus"
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
req.unicode-ansi: lineGetLineDevStatusW (Unicode) and lineGetLineDevStatusA (ANSI)
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
-	lineGetLineDevStatus
-	lineGetLineDevStatusA
-	lineGetLineDevStatusW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetLineDevStatusW function


## -description


The 
<b>lineGetLineDevStatus</b> function enables an application to query the specified open line device for its current status.


## -parameters




### -param hLine

Handle to the open line device to be queried.


### -param lpLineDevStatus

Pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>. Upon successful completion of the request, this structure is filled with the line's device status. Prior to calling 
<b>lineGetLineDevStatus</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL.




## -remarks



An application uses 
<b>lineGetLineDevStatus</b> to query the line device for its current line status. This status information applies globally to all addresses on the line device. Use 
<a href="https://msdn.microsoft.com/8d747aa5-05cc-4426-9d46-24bce6b4af26">lineGetAddressStatus</a> to determine status information about a specific address on a line.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/8d747aa5-05cc-4426-9d46-24bce6b4af26">lineGetAddressStatus</a>
 

 

