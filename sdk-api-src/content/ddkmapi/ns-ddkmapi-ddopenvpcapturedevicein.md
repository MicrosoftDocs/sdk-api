---
UID: NS:ddkmapi._DDOPENVPCAPTUREDEVICEIN
title: DDOPENVPCAPTUREDEVICEIN (ddkmapi.h)
description: The DDOPENVPCAPTUREDEVICEIN structure contains the video port extensions (VPE) capture information.
helpviewer_keywords: ["*LPDDOPENVPCAPTUREDEVICEIN","DDOPENVPCAPTUREDEVICEIN","DDOPENVPCAPTUREDEVICEIN structure [Display Devices]","LPDDOPENVPCAPTUREDEVICEIN","LPDDOPENVPCAPTUREDEVICEIN structure pointer [Display Devices]","ddkmapi/DDOPENVPCAPTUREDEVICEIN","ddkmapi/LPDDOPENVPCAPTUREDEVICEIN","ddstrcts_51a84e0d-3e5a-4ccc-93f1-bf3edfb29760.xml","display.ddopenvpcapturedevicein"]
old-location: display\ddopenvpcapturedevicein.htm
tech.root: display
ms.assetid: 75a2eaf7-a40f-4554-8dcf-f786d5771d43
ms.date: 12/05/2018
ms.keywords: '*LPDDOPENVPCAPTUREDEVICEIN, DDOPENVPCAPTUREDEVICEIN, DDOPENVPCAPTUREDEVICEIN structure [Display Devices], LPDDOPENVPCAPTUREDEVICEIN, LPDDOPENVPCAPTUREDEVICEIN structure pointer [Display Devices], ddkmapi/DDOPENVPCAPTUREDEVICEIN, ddkmapi/LPDDOPENVPCAPTUREDEVICEIN, ddstrcts_51a84e0d-3e5a-4ccc-93f1-bf3edfb29760.xml, display.ddopenvpcapturedevicein'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDOPENVPCAPTUREDEVICEIN, *LPDDOPENVPCAPTUREDEVICEIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDOPENVPCAPTUREDEVICEIN
 - ddkmapi/_DDOPENVPCAPTUREDEVICEIN
 - LPDDOPENVPCAPTUREDEVICEIN
 - ddkmapi/LPDDOPENVPCAPTUREDEVICEIN
 - DDOPENVPCAPTUREDEVICEIN
 - ddkmapi/DDOPENVPCAPTUREDEVICEIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDOPENVPCAPTUREDEVICEIN
---

# DDOPENVPCAPTUREDEVICEIN structure


## -description

The DDOPENVPCAPTUREDEVICEIN structure contains the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> capture information.

## -struct-fields

### -field hDirectDraw

Specifies the Microsoft DirectDraw handle from which the capture takes place.

### -field hVideoPort

Specifies the VPE object handle from which the capture takes place.

### -field dwStartLine

Indicates the starting line of the capture. This member is relative to the start of the surface (0 is the first line).

### -field dwEndLine

Indicates the last line of the capture (inclusive).

### -field dwCaptureEveryNFields

Contains a value that is the divisor for the number of fields that are to be captured per second. A field is a region that typically contains 240 lines, in which two fields make up a frame. Fields come at a rate of approximately 60 per second. To capture all 60 fields per second, set this value to 1, to capture 30 fields per second, set this value to 2, to capture 15 fields per second, set this field to 4, and so on.

### -field pfnCaptureClose

Points to a <a href="/windows/desktop/api/ddkmapi/nc-ddkmapi-lpdd_notifycallback">pfnCaptureClose</a> callback that is called when the capture device becomes unusable due to the VPE object being released at user mode.

### -field pContext

Contains the value that is passed if the <i>pfnCaptureClose</i> callback is ever called.

### -field dwFlags

One of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDOPENCAPTURE_VBI

</td>
<td>
Capture from the <a href="/windows-hardware/drivers/">VBI</a> stream.

</td>
</tr>
<tr>
<td>
DDOPENCAPTURE_VIDEO

</td>
<td>
Capture from the video stream.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff551500(v=vs.85)">DD_DXAPI_OPENVPCAPTUREDEVICE</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>