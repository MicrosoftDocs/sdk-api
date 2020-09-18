---
UID: NF:shellscalingapi.GetDpiForMonitor
title: GetDpiForMonitor function (shellscalingapi.h)
description: Queries the dots per inch (dpi) of a display.
helpviewer_keywords: ["GetDpiForMonitor","GetDpiForMonitor function [High DPI]","hidpi.getdpiformonitor","shellscalingapi/GetDpiForMonitor"]
old-location: hidpi\getdpiformonitor.htm
tech.root: hidpi
ms.assetid: AB741D14-0BA1-4C33-91D8-1331BE96DE95
ms.date: 12/05/2018
ms.keywords: GetDpiForMonitor, GetDpiForMonitor function [High DPI], hidpi.getdpiformonitor, shellscalingapi/GetDpiForMonitor
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shcore.lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetDpiForMonitor
 - shellscalingapi/GetDpiForMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - api-ms-win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-L1-1-2.dll
api_name:
 - GetDpiForMonitor
---

# GetDpiForMonitor function


## -description

Queries the dots per inch (dpi) of a display.

## -parameters

### -param hmonitor [in]

Handle of the monitor being queried.

### -param dpiType [in]

The type of DPI being queried. Possible values are from the <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-monitor_dpi_type">MONITOR_DPI_TYPE</a> enumeration.

### -param dpiX [out]

The value of the DPI along the X axis. This value always refers to the horizontal edge, even when the screen is rotated.

### -param dpiY [out]

The value of the DPI along the Y axis. This value always refers to the vertical edge, even when the screen is rotated.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function successfully returns the X and Y DPI values for the specified monitor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle, DPI type, or pointers passed in are not valid.

</td>
</tr>
</table>

## -remarks

This API is not DPI aware and should not be used if the calling thread is per-monitor DPI aware. For the DPI-aware version of this API, see <a href="/windows/desktop/api/winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a>.

When you call <b>GetDpiForMonitor</b>, you will receive different DPI values depending on the DPI awareness of the calling application. DPI awareness is an application-level property usually defined in the application manifest. For more information about DPI awareness values, see <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>. The following table indicates how the results will differ based on the <b>PROCESS_DPI_AWARENESS</b> value of your application.

<table>
<tr>
<td><b>PROCESS_DPI_UNAWARE</b></td>
<td>96 because the app is unaware of any other scale factors.</td>
</tr>
<tr>
<td><b>PROCESS_SYSTEM_DPI_AWARE</b></td>
<td>A value set to the system DPI because the app assumes all applications use the system DPI.</td>
</tr>
<tr>
<td><b>PROCESS_PER_MONITOR_DPI_AWARE</b></td>
<td>The actual DPI value set by the user for that display.</td>
</tr>
</table>
 

The values of <i>*dpiX</i> and <i>*dpiY</i> are identical. You only need to record one of the values to determine the DPI and respond appropriately.

When <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-monitor_dpi_type">MONITOR_DPI_TYPE</a> is <b>MDT_ANGULAR_DPI</b> or <b>MDT_RAW_DPI</b>, the returned DPI value does not include any changes that the user made to the DPI by using the desktop scaling override slider control in Control Panel.

For more information about DPI settings in Control Panel, see the <a href="/windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">Writing DPI-Aware Desktop Applications in Windows 8.1 Preview</a> white paper.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>