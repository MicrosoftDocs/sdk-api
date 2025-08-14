---
UID: NF:winuser.FlashWindowEx
title: FlashWindowEx function (winuser.h)
description: Flashes the specified window. It does not change the active state of the window.
helpviewer_keywords: ["FlashWindowEx","FlashWindowEx function","_win32_flashwindowex","base.flashwindowex","winuser/FlashWindowEx"]
old-location: base\flashwindowex.htm
tech.root: Debug
ms.assetid: 474ec2d9-3ee9-4622-843e-d6ae36fedd7f
ms.date: 12/05/2018
ms.keywords: FlashWindowEx, FlashWindowEx function, _win32_flashwindowex, base.flashwindowex, winuser/FlashWindowEx
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - FlashWindowEx
 - winuser/FlashWindowEx
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
 - User32.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - FlashWindowEx
req.apiset: ext-ms-win-ntuser-misc-l1-5-0 (introduced in Windows 10, version 10.0.10240)
---

# FlashWindowEx function


## -description

Flashes the specified window. It does not change the active state of the window.

## -parameters

### -param pfwi [in]

A pointer to a 
<a href="/windows/desktop/api/winuser/ns-winuser-flashwinfo">FLASHWINFO</a> structure.

## -returns

The return value specifies the window's state before the call to the 
<b>FlashWindowEx</b> function. If the window caption was drawn as active before the call, the return value is nonzero. Otherwise, the return value is zero.

## -remarks

Typically, you flash a window to inform the user that the window requires attention but does not currently have the keyboard focus. When a window flashes, it appears to change from inactive to active status. An inactive caption bar changes to an active caption bar; an active caption bar changes to an inactive caption bar.

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/api/winuser/ns-winuser-flashwinfo">FLASHWINFO</a>



<a href="/windows/desktop/Debug/notifying-the-user">Notifying the User</a>
