---
UID: NF:shellscalingapi.SetProcessDpiAwareness
title: SetProcessDpiAwareness function (shellscalingapi.h)
description: Sets the process-default DPI awareness level. This is equivalent to calling SetProcessDpiAwarenessContext with the corresponding DPI_AWARENESS_CONTEXT value.
helpviewer_keywords: ["SetProcessDpiAwareness","SetProcessDpiAwareness function [High DPI]","hidpi.setprocessdpiawareness","shellscalingapi/SetProcessDpiAwareness","winmsg.SetProcessDpiAwareness"]
old-location: hidpi\setprocessdpiawareness.htm
tech.root: hidpi
ms.assetid: BFD64207-D35D-4258-982C-20D6FE2B46F9
ms.date: 12/05/2018
ms.keywords: SetProcessDpiAwareness, SetProcessDpiAwareness function [High DPI], hidpi.setprocessdpiawareness, shellscalingapi/SetProcessDpiAwareness, winmsg.SetProcessDpiAwareness
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
 - SetProcessDpiAwareness
 - shellscalingapi/SetProcessDpiAwareness
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
 - SetProcessDpiAwareness
---

# SetProcessDpiAwareness function


## -description

Sets the process-default DPI awareness level. This is equivalent to calling <a href="/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext">SetProcessDpiAwarenessContext</a> with the corresponding <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> value.

> [!NOTE]
> It is recommended that you set the process-default DPI awareness via application manifest, not an API call. See <a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.

## -parameters

### -param value [in]

The DPI awareness value to set. Possible values are from the <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a> enumeration.

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
The DPI awareness for the app was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The DPI awareness is already set, either by calling this API previously or through the application (.exe) manifest.

</td>
</tr>
</table>

## -remarks

Previous versions of Windows only had one DPI awareness value for the entire application. For those applications, the recommendation was to set the DPI awareness value in the manifest as described in <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>. Under that recommendation, you were not supposed to use <b>SetProcessDpiAwareness</b> to update the DPI awareness. In fact, future calls  to this API would fail after the DPI awareness was set once. Now that DPI awareness is tied to a thread rather than an application, you can use this method to update the DPI awareness. However, consider using <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a> instead.

<div class="alert"><b>Important</b>  <p class="note">For older applications, it is strongly recommended to not use <b>SetProcessDpiAwareness</b> to set the DPI awareness for your application. Instead, you should declare the DPI awareness for your application in the application manifest. See <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a> for more information about the DPI awareness values and how to set them in the manifest.

</div>
<div> </div>
You must call this API before you call any APIs that depend on the dpi awareness. This is part of the reason why it is recommended to use the application manifest rather than the <b>SetProcessDpiAwareness</b> API. Once API awareness is set for an app, any future calls to this API will fail. This is true regardless of whether you set the DPI awareness in the manifest or by using this API.

If the DPI awareness level is not set, the default value is <b>PROCESS_DPI_UNAWARE</b>.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">PROCESS_DPI_AWARENESS</a>

<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>

<a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a>
