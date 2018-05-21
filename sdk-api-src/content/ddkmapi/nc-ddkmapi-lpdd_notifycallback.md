---
UID: NC:ddkmapi.LPDD_NOTIFYCALLBACK
title: LPDD_NOTIFYCALLBACK
author: windows-driver-content
description: The NotifyCallback callback function performs operations related to an event that occurred.
old-location: display\notifycallback.htm
old-project: display
ms.assetid: ee581d7b-c3b8-47e5-bae8-348b22ea0f95
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: LPDD_NOTIFYCALLBACK, LPDD_NOTIFYCALLBACK callback, NotifyCallback, NotifyCallback callback function [Display Devices], ddfncs_89344672-ba6d-42b3-a03e-dd832316d9c9.xml, ddkmapi/NotifyCallback, display.notifycallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
req.target-type: Desktop
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
req.typenames: "*LPDDKERNELCAPS, DDKERNELCAPS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddkmapi.h
api_name:
-	NotifyCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# LPDD_NOTIFYCALLBACK callback function


## -description


The<i> NotifyCallback</i> callback function performs operations related to an event that occurred.


## -parameters




### -param dwFlags

Indicates the event that caused the callback to be called. The values in <i>dwParam1</i> and <i>dwParam2</i> depend on the value of <i>dwFlags</i>. The following values are possible:

<table>
<tr>
<th>Flag</th>
<th><i>dwParam1</i></th>
<th><i>dwParam2</i></th>
</tr>
<tr>
<td>
DDNOTIFY_CLOSECAPTURE

</td>
<td>
hCapture

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_CLOSEDIRECTDRAW

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_CLOSESURFACE

</td>
<td>
hSurface

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_CLOSEVIDEOPORT

</td>
<td>
hVideoPort

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_DISPLAY_VSYNC

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_POSTDOSBOX

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_POSTRESCHANGE

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_PREDOSBOX

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_PRERESCHANGE

</td>
<td>
hDirectDraw

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_VP_LINE

</td>
<td>
hVideoPort

</td>
<td>
unused

</td>
</tr>
<tr>
<td>
DDNOTIFY_VP_VSYNC

</td>
<td>
hVideoPort

</td>
<td>
unused

</td>
</tr>
</table>
 


### -param pContext

Contains a value that the caller passed in a call to the <b>DxApi</b> function along with a specific function identifier. For more information about function identifiers, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>.


### -param dwParam1

Handle to the object related to the event that caused the callback to be called. 


### -param dwParam2

Unused.


## -returns



<i>NotifyCallback</i> returns zero.




## -remarks



A video capture driver supplies a <i>NotifyCallback</i> callback function to the DirectDraw runtime when the video capture driver calls the runtime's <a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a> function. For more information, see <a href="https://msdn.microsoft.com/2b900436-7874-43a7-97bf-7d1eead78126">Notify Callback Functions in a Video Capture Driver</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550252">DDOPENDIRECTDRAWIN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550254">DDOPENDIRECTDRAWOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550257">DDOPENSURFACEIN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550261">DDOPENSURFACEOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550265">DDOPENVIDEOPORTIN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550267">DDOPENVIDEOPORTOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550269">DDOPENVPCAPTUREDEVICEIN</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550272">DDOPENVPCAPTUREDEVICEOUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550283">DDREGISTERCALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550702">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550711">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551498">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551500">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551502">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

