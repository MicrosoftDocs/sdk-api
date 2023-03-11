---
UID: NE:shellscalingapi.PROCESS_DPI_AWARENESS
title: PROCESS_DPI_AWARENESS (shellscalingapi.h)
description: Identifies dots per inch (dpi) awareness values. DPI awareness indicates how much scaling work an application performs for DPI versus how much is done by the system.
helpviewer_keywords: ["PROCESS_DPI_AWARENESS","PROCESS_DPI_AWARENESS enumeration [High DPI]","PROCESS_DPI_UNAWARE","PROCESS_PER_MONITOR_DPI_AWARE","PROCESS_SYSTEM_DPI_AWARE","hidpi.process_dpi_awareness","shellscalingapi/PROCESS_DPI_AWARENESS","shellscalingapi/PROCESS_DPI_UNAWARE","shellscalingapi/PROCESS_PER_MONITOR_DPI_AWARE","shellscalingapi/PROCESS_SYSTEM_DPI_AWARE"]
old-location: hidpi\process_dpi_awareness.htm
tech.root: hidpi
ms.assetid: 50130739-E8A8-4B92-9B80-3BBBE57EBE0C
ms.date: 12/05/2018
ms.keywords: PROCESS_DPI_AWARENESS, PROCESS_DPI_AWARENESS enumeration [High DPI], PROCESS_DPI_UNAWARE, PROCESS_PER_MONITOR_DPI_AWARE, PROCESS_SYSTEM_DPI_AWARE, hidpi.process_dpi_awareness, shellscalingapi/PROCESS_DPI_AWARENESS, shellscalingapi/PROCESS_DPI_UNAWARE, shellscalingapi/PROCESS_PER_MONITOR_DPI_AWARE, shellscalingapi/PROCESS_SYSTEM_DPI_AWARE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROCESS_DPI_AWARENESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROCESS_DPI_AWARENESS
 - shellscalingapi/PROCESS_DPI_AWARENESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ShellScalingApi.h
api_name:
 - PROCESS_DPI_AWARENESS
---

# PROCESS_DPI_AWARENESS enumeration


## -description

Identifies dots per inch (dpi) awareness values. DPI awareness indicates how much scaling work an application performs for DPI versus how much is done by the system.

Users have the ability to set the DPI scale factor on their displays independent of each other. Some legacy applications are not able to adjust their scaling for multiple DPI settings. In order for users to use these applications without content appearing too large or small on displays, Windows can apply DPI virtualization to an application, causing it to be automatically scaled by the system to match the DPI of the current display. The <b>PROCESS_DPI_AWARENESS</b> value indicates what level of scaling your application handles on its own and how much is provided by Windows. Keep in mind that applications scaled by the system may appear blurry and will read virtualized data about the monitor to maintain compatibility.

## -enum-fields

### -field PROCESS_DPI_UNAWARE:0

DPI unaware. This app does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI). It will be automatically scaled by the system on any other DPI setting.

### -field PROCESS_SYSTEM_DPI_AWARE:1

System DPI aware. This app does not scale for DPI changes. It will query for the DPI once and use that value for the lifetime of the app. If the DPI changes, the app will not adjust to the new DPI value. It will be automatically scaled up or down by the system when the DPI changes from the system value.

### -field PROCESS_PER_MONITOR_DPI_AWARE:2

Per monitor DPI aware. This app checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes. These applications are not automatically scaled by the system.

## -remarks

<div class="alert"><b>Important</b>  <p class="note">Previous versions of Windows required you to set the DPI awareness for the entire application. Now the DPI awareness is tied to individual threads, processes, or windows. This means that the DPI awareness can change while the app is running and that multiple windows can have their own independent DPI awareness values. See <a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a> for more information about how DPI awareness currently works. The recommendations below about setting the DPI awareness in the application manifest are still supported, but the current recommendation is to use the <b>DPI_AWARENESS_CONTEXT</b>.

</div>
<div> </div>
The DPI awareness for an application should be set through the application manifest so that it is determined before any actions are taken which depend on the DPI of the system. Alternatively, you can set the DPI awareness using <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness">SetProcessDpiAwareness</a>, but if you do so, you need to make sure to set it before taking any actions dependent on the system DPI. Once you set the DPI awareness for a process, it cannot be changed.

<div class="alert"><b>Tip</b>  <p class="note">If your app is <b>PROCESS_DPI_UNAWARE</b>, there is no need to set any value in the application manifest. <b>PROCESS_DPI_UNAWARE</b> is the default value for apps unless another value is specified.

</div>
<div> </div>
<b>PROCESS_DPI_UNAWARE</b> and <b>PROCESS_SYSTEM_DPI_AWARE</b> apps do not need to respond to <a href="/windows/desktop/hidpi/wm-dpichanged">WM_DPICHANGED</a> and are not expected to handle changes in DPI. The system will automatically scale these types of apps up or down as necessary when the DPI changes. <b>PROCESS_PER_MONITOR_DPI_AWARE</b> apps are responsible for recognizing and responding to changes in DPI, signaled by <b>WM_DPICHANGED</b>. These will not be scaled by the system. If an app of this type does not resize the window and its content,  it will appear to grow or shrink by the relative DPI changes as the window is moved from one display to the another with a different DPI setting.

<div class="alert"><b>Tip</b>  <p class="note">In previous versions of Windows, there was no setting for <b>PROCESS_PER_MONITOR_DPI_AWARE</b>. Apps were either DPI unaware or DPI aware. Legacy applications that were classified as DPI aware before Windows 8.1 are considered to have a <b>PROCESS_DPI_AWARENESS</b> setting of <b>PROCESS_SYSTEM_DPI_AWARE</b> in current versions of Windows.

</div>
<div> </div>
To understand the importance and impact of the different DPI awareness values, consider a user who has three displays: A, B, and C. Display A is set to 100% scaling factor (96 DPI), display B is set to 200% scaling factor (192 DPI), and display C is set to 300% scaling factor (288 DPI). The system DPI is set to 200%.

An application that is <b>PROCESS_DPI_UNAWARE</b> will always use a scaling factor of 100% (96 DPI). In this scenario, a <b>PROCESS_DPI_UNAWARE</b> window is created with a size of 500 by 500. On display A, it will render natively with no scaling. On displays B and C, it will be scaled up by the system automatically by a factor of 2 and 3 respectively. This is because a <b>PROCESS_DPI_UNAWARE</b> always assumes a DPI of 96, and the system accounts for that. If the app queries for window size, it will always get a value of 500 by 500 regardless of what display it is in. If this app were to ask for the DPI of any of the three monitors, it will receive 96.

Now consider an application that is <b>PROCESS_SYSTEM_DPI_AWARE</b>. Remember that in the sample, the system DPI is 200% or 192 DPI. This means that any windows created by this app will render natively on display B. It the window moves to display A, it will automatically be scaled down by a factor of 2. This is because a <b>PROCESS_SYSTEM_DPI_AWARE</b> app in this scenario assumes that the DPI will always be 192. It queries for the DPI on startup, and then never changes it. The system accommodates this by automatically scaling down when moving to display A. Likewise, if the window moves to display C, the system will automatically scale up by a factor of 1.5. If the app queries for window size, it will always get the same value, similar to <b>PROCESS_DPI_UNAWARE</b>. If it asks for the DPI of any of the three monitors, it will receive 192.

Unlike the other awareness values, <b>PROCESS_PER_MONITOR_DPI_AWARE</b> should adapt to the display that it is on. This means that it is always rendered natively and is never scaled by the system. The responsibility is on the app to adjust the scale factor when receiving the <a href="/windows/desktop/hidpi/wm-dpichanged">WM_DPICHANGED</a> message. Part of this message includes a suggested rect for the window. This suggestion is the current window scaled from the old DPI value to the new DPI value. For example, a window that is 500 by 500 on display A and moved to display B will receive a suggested window rect that is 1000 by 1000. If that same window is moved to display C, the suggested window rect attached to <b>WM_DPICHANGED</b> will be 1500 by 1500. Furthermore, when this app queries for the window size, it will always get the actual native value. Likewise, if it asks for the DPI of any of the three monitors, it will receive 96, 192, and 288 respectively.

Because of DPI virtualization, if one application queries another with a different awareness level for DPI-dependent information, the system will automatically scale values to match the awareness level of the caller. One example of this is if you call <a href="/windows/desktop/api/winuser/nf-winuser-getwindowrect">GetWindowRect</a> and pass in a window created by another application. Using the situation described above, assume that a <b>PROCESS_DPI_UNAWARE</b> app created a 500 by 500 window on display C. If you query for the window rect from a different application, the size of the rect will vary based upon the DPI awareness of your app.<table>
<tr>
<td><b>PROCESS_DPI_UNAWARE</b></td>
<td>You will get a 500 by 500 rect because the system will assume a DPI of 96 and automatically scale the actual rect down by a factor of 3.</td>
</tr>
<tr>
<td><b>PROCESS_SYSTEM_DPI_AWARE</b></td>
<td>You will get a 1000 by 1000 rect because the system will assume a DPI of 192 and automatically scale the actual rect down by a factor of 3/2.</td>
</tr>
<tr>
<td><b>PROCESS_PER_MONITOR_DPI_AWARE</b></td>
<td>You will get a 1500 by 1500 rect because the system will use the actual DPI of the display and not do any scaling behind the scenes.</td>
</tr>
</table>
 




#### Examples

This snippet demonstrates how to set a value of <b>PROCESS_SYSTEM_DPI_AWARE</b> in your application manifest.


```xml
<dpiAware>true</dpiAware>
```


This snippet demonstrates how to set a value of <b>PROCESS_PER_MONITOR_DPI_AWARE</b> in your application manifest.


```xml
<dpiAware>true/PM</dpiAware>
```

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_awareness">DPI_AWARENESS</a>
