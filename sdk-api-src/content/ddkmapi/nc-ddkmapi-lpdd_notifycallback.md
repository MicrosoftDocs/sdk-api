---
UID: NC:ddkmapi.LPDD_NOTIFYCALLBACK
title: LPDD_NOTIFYCALLBACK (ddkmapi.h)
description: The NotifyCallback callback function performs operations related to an event that occurred.
helpviewer_keywords: ["LPDD_NOTIFYCALLBACK","LPDD_NOTIFYCALLBACK callback","NotifyCallback","NotifyCallback callback function [Display Devices]","ddfncs_89344672-ba6d-42b3-a03e-dd832316d9c9.xml","ddkmapi/NotifyCallback","display.notifycallback"]
old-location: display\notifycallback.htm
tech.root: display
ms.assetid: ee581d7b-c3b8-47e5-bae8-348b22ea0f95
ms.date: 12/05/2018
ms.keywords: LPDD_NOTIFYCALLBACK, LPDD_NOTIFYCALLBACK callback, NotifyCallback, NotifyCallback callback function [Display Devices], ddfncs_89344672-ba6d-42b3-a03e-dd832316d9c9.xml, ddkmapi/NotifyCallback, display.notifycallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDD_NOTIFYCALLBACK
 - ddkmapi/LPDD_NOTIFYCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddkmapi.h
api_name:
 - NotifyCallback
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

Contains a value that the caller passed in a call to the <b>DxApi</b> function along with a specific function identifier. For more information about function identifiers, see <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>.

### -param dwParam1

Handle to the object related to the event that caused the callback to be called.

### -param dwParam2

Unused.

## -returns

<i>NotifyCallback</i> returns zero.

## -remarks

A video capture driver supplies a <i>NotifyCallback</i> callback function to the DirectDraw runtime when the video capture driver calls the runtime's <a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a> function. For more information, see <a href="/windows-hardware/drivers/display/notify-callback-functions-in-a-video-capture-driver">Notify Callback Functions in a Video Capture Driver</a>.

## -see-also

<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopendirectdrawin">DDOPENDIRECTDRAWIN</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopendirectdrawout">DDOPENDIRECTDRAWOUT</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopensurfacein">DDOPENSURFACEIN</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopensurfaceout">DDOPENSURFACEOUT</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopenvideoportin">DDOPENVIDEOPORTIN</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopenvideoportout">DDOPENVIDEOPORTOUT</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopenvpcapturedevicein">DDOPENVPCAPTUREDEVICEIN</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddopenvpcapturedeviceout">DDOPENVPCAPTUREDEVICEOUT</a>



<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddregistercallback">DDREGISTERCALLBACK</a>



<a href="/previous-versions/windows/hardware/drivers/ff550702(v=vs.85)">DD_DXAPI_OPENDIRECTDRAW</a>



<a href="/previous-versions/windows/hardware/drivers/ff550711(v=vs.85)">DD_DXAPI_OPENSURFACE</a>



<a href="/previous-versions/windows/hardware/drivers/ff551498(v=vs.85)">DD_DXAPI_OPENVIDEOPORT</a>



<a href="/previous-versions/windows/hardware/drivers/ff551500(v=vs.85)">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="/previous-versions/windows/hardware/drivers/ff551502(v=vs.85)">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>