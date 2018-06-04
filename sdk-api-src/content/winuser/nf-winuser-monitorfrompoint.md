---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MonitorFromPoint function


## -description


The <b>MonitorFromPoint</b> function retrieves a handle to the display monitor that contains a specified point.


## -parameters




### -param pt [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that specifies the point of interest in virtual-screen coordinates.


### -param dwFlags [in]

Determines the function's return value if the point is not contained within any display monitor.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONEAREST"></a><a id="monitor_defaulttonearest"></a><dl>
<dt><b>MONITOR_DEFAULTTONEAREST</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the display monitor that is nearest to the point.

</td>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONULL"></a><a id="monitor_defaulttonull"></a><dl>
<dt><b>MONITOR_DEFAULTTONULL</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTOPRIMARY"></a><a id="monitor_defaulttoprimary"></a><dl>
<dt><b>MONITOR_DEFAULTTOPRIMARY</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the primary display monitor.

</td>
</tr>
</table>
 


## -returns



If the point is contained by a display monitor, the return value is an <b>HMONITOR</b> handle to that display monitor.

If the point is not contained by a display monitor, the return value depends on the value of <i>dwFlags</i>.




## -see-also




<a href="https://msdn.microsoft.com/81c3fffb-bbc9-4adb-bb6b-edd59f7a77b4">MonitorFromRect</a>



<a href="https://msdn.microsoft.com/fe6505c9-b481-4fec-ae9d-995943234a3a">MonitorFromWindow</a>



<a href="https://msdn.microsoft.com/a64b256c-e7a1-4ee2-a346-4b7abcab9e90">Multiple Display Monitors Functions</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>
 

 

