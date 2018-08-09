---
UID: NS:tapi.linedevstatus_tag
title: linedevstatus_tag
author: windows-sdk-content
description: The LINEDEVSTATUS structure describes the current status of a line device. The lineGetLineDevStatus function and the TSPI_lineGetLineDevStatus function return the LINEDEVSTATUS structure.
old-location: tapi2\linedevstatus_str.htm
old-project: tapi
ms.assetid: 3d565e99-eb90-47ca-9fb9-295236f566fb
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "*LPLINEDEVSTATUS, LINEDEVSTATUS, LINEDEVSTATUS structure [TAPI 2.2], LPLINEDEVSTATUS, LPLINEDEVSTATUS structure pointer [TAPI 2.2], _tapi2_linedevstatus_str, linedevstatus_tag, tapi/LINEDEVSTATUS, tapi/LPLINEDEVSTATUS, tapi2.linedevstatus_str"
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
req.typenames: LINEDEVSTATUS, *LPLINEDEVSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEDEVSTATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linedevstatus_tag structure


## -description


The 
<b>LINEDEVSTATUS</b> structure describes the current status of a line device. The 
<a href="https://msdn.microsoft.com/9c0fa2ba-1157-43d2-af56-aa4e0c28bd05">lineGetLineDevStatus</a> function and the 
<a href="https://msdn.microsoft.com/14f7944b-e967-4967-9fb2-e7aeb78bb045">TSPI_lineGetLineDevStatus</a> function return the 
<b>LINEDEVSTATUS</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumOpens

Number of active opens on the line device.


### -field dwOpenMediaModes

Bit array that indicates for which media types the line device is currently open.


### -field dwNumActiveCalls

Number of calls on the line in call states other than <i>idle</i>, <i>onhold</i>, <i>onholdpendingtransfer</i>, and <i>onholdpendingconference</i>.


### -field dwNumOnHoldCalls

Number of calls on the line in the <i>onhold</i> state.


### -field dwNumOnHoldPendCalls

Number of calls on the line in the <i>onholdpendingtransfer</i> or <i>onholdpendingconference</i> state.


### -field dwLineFeatures

Line-related functions that are currently available on this line. This member uses one or more of the 
<a href="https://msdn.microsoft.com/77fa313c-e720-4607-b691-51b5be76ceed">LINEFEATURE_ Constants</a>.


### -field dwNumCallCompletions

Number of outstanding call completion requests on the line.


### -field dwRingMode

Current ring mode on the line device.


### -field dwSignalLevel

Current signal level of the connection on the line. This is a value in the range 0x00000000 (weakest signal) to 0x0000FFFF (strongest signal).


### -field dwBatteryLevel

Current battery level of the line device hardware. This is a value in the range 0x00000000 (battery empty) to 0x0000FFFF (battery full).


### -field dwRoamMode

Current roam mode of the line device. This member uses one of the 
<a href="https://msdn.microsoft.com/af0eb263-8deb-44ab-8acb-00e4ff7930ab">LINEROAMMODE_ Constants</a>.


### -field dwDevStatusFlags

Flags that indicate status information, such as whether the device is locked. It consists of one or more members of 
<a href="https://msdn.microsoft.com/5fa754d3-07b2-4b75-91ef-1bf961d9fef4">LINEDEVSTATUSFLAGS_ Constants</a>.


### -field dwTerminalModesSize

Size of the variably-sized device field containing an array of current terminal modes, in bytes.


### -field dwTerminalModesOffset

Offset from the beginning of the structure to an array of current terminal modes, in bytes. This array is indexed by terminal IDs, in the range from zero to <b>dwNumTerminals</b> minus one. Each entry in the array specifies the current terminal modes for the corresponding terminal set using the 
<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a> function for this line. Each entry is a <b>DWORD</b> that specifies one or more of the 
<a href="https://msdn.microsoft.com/60af1687-8958-4918-be21-a13780c60974">LINETERMMODE_ Constants</a>. The size of the array is specified by <b>dwTerminalModesSize</b>.


### -field dwDevSpecificSize

Size of the variably sized device-specific field, in bytes. If the device-specific information is a pointer to a string, the size must include the <b>null</b> terminator. 


### -field dwDevSpecificOffset

Offset from the beginning of the structure to the device-specific field, in bytes. The size of the field is specified by <b>dwDevSpecificSize</b>.


### -field dwAvailableMediaModes

Indicates the media types that can be invoked on new calls created on this line device, when the <b>dwLineFeatures</b> member indicates that new calls are possible. If this member is zero, it indicates that the service provider either does not know or cannot indicate which media types are available, in which case any or all of the media types indicated in the <b>dwMediaModes</b> member in 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> may be available.


### -field dwAppInfoSize

Size of the array that identifies the applications that have the line open, in bytes.


### -field dwAppInfoOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/1c1d2d31-a234-407e-b9fc-4823928c5ca1">LINEAPPINFO</a> structures. The <b>dwNumOpens</b> member indicates the number of elements in the array. Each element in the array identifies an application that has the line open. The size of the array is specified by <b>dwAppInfoSize</b>.


## -remarks



Device-specific extensions should use the DevSpecific (<b>dwDevSpecificSize</b> and <b>dwDevSpecificOffset</b>) variably sized area of this data structure.

The members <b>dwAvailableMediaModes</b> through <b>dwAppInfoOffset</b> are available only to applications that open the line device with an API version of 2.0 or later.




## -see-also




<a href="https://msdn.microsoft.com/1c1d2d31-a234-407e-b9fc-4823928c5ca1">LINEAPPINFO</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/14f7944b-e967-4967-9fb2-e7aeb78bb045">TSPI_lineGetLineDevStatus</a>



<a href="https://msdn.microsoft.com/9c0fa2ba-1157-43d2-af56-aa4e0c28bd05">lineGetLineDevStatus</a>



<a href="https://msdn.microsoft.com/362114d9-c5b6-4b78-bb31-811eb89fe82d">lineSetTerminal</a>
 

 

