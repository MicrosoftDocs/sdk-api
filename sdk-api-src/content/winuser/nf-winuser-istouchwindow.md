---
UID: NF:winuser.IsTouchWindow
title: IsTouchWindow function (winuser.h)
description: Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.
helpviewer_keywords: ["IsTouchWindow","IsTouchWindow function [Windows Touch]","wintouch.istouchwindow","winuser/IsTouchWindow"]
old-location: wintouch\istouchwindow.htm
tech.root: wintouch
ms.assetid: 080b9d18-5975-4d38-ae3b-151f74120bb3
ms.date: 12/05/2018
ms.keywords: IsTouchWindow, IsTouchWindow function [Windows Touch], wintouch.istouchwindow, winuser/IsTouchWindow
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsTouchWindow
 - winuser/IsTouchWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - IsTouchWindow
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# IsTouchWindow function


## -description

Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.

## -parameters

### -param hwnd [in]

The handle of the window. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread is not on the same desktop as the specified window.

### -param pulFlags [out, optional]

The address of the <b>ULONG</b> variable to receive the modifier flags for the specified window's touch capability.

## -returns

Returns <b>TRUE</b> if the window supports Windows Touch; returns <b>FALSE</b> if the window does not support Windows Touch.

## -remarks

The following table lists the values for the <i>pulFlags</i> output parameter.
		

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>TWF_FINETOUCH</b></td>
<td>Specifies that <i>hWnd</i> prefers noncoalesced touch input.</td>
</tr>
<tr>
<td><b>TWF_WANTPALM</b></td>
<td>
Clearing this flag disables palm rejection which reduces delays for getting <a href="/windows/desktop/wintouch/wm-touchdown">WM_TOUCH</a> messages. 
						     This is useful if you want as quick of a response as possible when a user touches your application.
						  

Setting this flag enables palm detection and will prevent some <a href="/windows/desktop/wintouch/wm-touchdown">WM_TOUCH</a> messages from being sent 
						     to your application.  This is useful if you do not want to receive <b>WM_TOUCH</b> messages that are from palm contact.
                    

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wintouch/mtfunctions">Functions</a>
