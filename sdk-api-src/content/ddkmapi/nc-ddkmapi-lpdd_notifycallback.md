---
UID: NC:ddkmapi.LPDD_NOTIFYCALLBACK
title: LPDD_NOTIFYCALLBACK
author: windows-sdk-content
description: The NotifyCallback callback function performs operations related to an event that occurred.
old-location: display\notifycallback.htm
tech.root: display
ms.assetid: ee581d7b-c3b8-47e5-bae8-348b22ea0f95
ms.author: windowssdkdev
ms.date: 11/15/2018
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddkmapi.h
api_name:
 - NotifyCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Contains a value that the caller passed in a call to the <b>DxApi</b> function along with a specific function identifier. For more information about function identifiers, see <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>.


### -param dwParam1

Handle to the object related to the event that caused the callback to be called. 


### -param dwParam2

Unused.


## -returns



<i>NotifyCallback</i> returns zero.




## -remarks



A video capture driver supplies a <i>NotifyCallback</i> callback function to the DirectDraw runtime when the video capture driver calls the runtime's <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function. For more information, see <a href="https://msdn.microsoft.com/2b900436-7874-43a7-97bf-7d1eead78126">Notify Callback Functions in a Video Capture Driver</a>.




## -see-also




<a href="https://msdn.microsoft.com/62a15685-5420-46cf-ae50-14bb8d97a3ce">DDOPENDIRECTDRAWIN</a>



<a href="https://msdn.microsoft.com/49fa1354-2b66-4e97-a8e6-aa7c995d6628">DDOPENDIRECTDRAWOUT</a>



<a href="https://msdn.microsoft.com/98a5d436-096d-4698-8f2c-31a0455300ff">DDOPENSURFACEIN</a>



<a href="https://msdn.microsoft.com/0cf0db38-f512-4ca1-a386-5544a1c9433e">DDOPENSURFACEOUT</a>



<a href="https://msdn.microsoft.com/53a0fdb3-583d-4da2-939c-6640ca9e6c31">DDOPENVIDEOPORTIN</a>



<a href="https://msdn.microsoft.com/cb01786f-4e6a-43f6-b906-504c0f17ade7">DDOPENVIDEOPORTOUT</a>



<a href="https://msdn.microsoft.com/75a2eaf7-a40f-4554-8dcf-f786d5771d43">DDOPENVPCAPTUREDEVICEIN</a>



<a href="https://msdn.microsoft.com/5979ccd5-7c35-4088-96b3-15e4416d5471">DDOPENVPCAPTUREDEVICEOUT</a>



<a href="https://msdn.microsoft.com/35b82122-0cff-4a19-9723-28ce38896f2a">DDREGISTERCALLBACK</a>



<a href="https://msdn.microsoft.com/57e543e3-071c-4d3f-80ee-99648d34737d">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="https://msdn.microsoft.com/b2449bf4-d7ef-440e-ae1f-6ede2895b831">DD_DXAPI_OPENSURFACE</a>



<a href="https://msdn.microsoft.com/a54335f1-fc08-447a-ba65-f1d99ba7924d">DD_DXAPI_OPENVIDEOPORT</a>



<a href="https://msdn.microsoft.com/3bd696a4-1a46-482b-9680-7cd1256904ae">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="https://msdn.microsoft.com/62132334-8989-48cb-919e-a236d2c53683">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

