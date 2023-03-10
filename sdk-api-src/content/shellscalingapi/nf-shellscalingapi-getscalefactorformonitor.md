---
UID: NF:shellscalingapi.GetScaleFactorForMonitor
title: GetScaleFactorForMonitor function (shellscalingapi.h)
description: Gets the scale factor of a specific monitor. This function replaces GetScaleFactorForDevice.
helpviewer_keywords: ["GetScaleFactorForMonitor","GetScaleFactorForMonitor function [Windows Shell]","shell.GetScaleFactorForMonitor","shellscalingapi/GetScaleFactorForMonitor"]
old-location: shell\GetScaleFactorForMonitor.htm
tech.root: shell
ms.assetid: 2F214512-704D-41A2-86A6-1EF880CD3DB4
ms.date: 12/05/2018
ms.keywords: GetScaleFactorForMonitor, GetScaleFactorForMonitor function [Windows Shell], shell.GetScaleFactorForMonitor, shellscalingapi/GetScaleFactorForMonitor
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
 - GetScaleFactorForMonitor
 - shellscalingapi/GetScaleFactorForMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - GetScaleFactorForMonitor
---

# GetScaleFactorForMonitor function


## -description

Gets the scale factor of a specific monitor. This function replaces <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorfordevice">GetScaleFactorForDevice</a>.

## -parameters

### -param hMon [in]

The monitor's handle.

### -param pScale [out]

When this function returns successfully, this value points to one of the <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">DEVICE_SCALE_FACTOR</a> values that specify the scale factor of the specified monitor.
                        

If the function call fails, this value points to a valid scale factor so that apps can opt to continue on with incorrectly sized resources.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Your code needs to handle the <a href="/windows/desktop/winmsg/wm-windowposchanged">WM_WINDOWPOSCHANGED</a> message in addition to the scale change event registered through <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>, because the app window can be moved between monitors. In response to the <b>WM_WINDOWPOSCHANGED</b> message, call <a href="/windows/desktop/api/winuser/nf-winuser-monitorfromwindow">MonitorFromWindow</a>, followed by <b>GetScaleFactorForMonitor</b> to get the scale factor of the monitor which the app window is on. Your code can then react to any dots per inch (dpi) change by reloading assets and changing layout.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>