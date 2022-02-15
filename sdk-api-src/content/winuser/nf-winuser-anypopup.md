---
UID: NF:winuser.AnyPopup
title: AnyPopup function (winuser.h)
description: Indicates whether an owned, visible, top-level pop-up, or overlapped window exists on the screen. The function searches the entire screen, not just the calling application's client area.
helpviewer_keywords: ["AnyPopup","AnyPopup function [Windows and Messages]","_win32_AnyPopup","_win32_anypopup_cpp","winmsg.anypopup","winui._win32_anypopup","winuser/AnyPopup"]
old-location: winmsg\anypopup.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\anypopup.htm
ms.date: 12/05/2018
ms.keywords: AnyPopup, AnyPopup function [Windows and Messages], _win32_AnyPopup, _win32_anypopup_cpp, winmsg.anypopup, winui._win32_anypopup, winuser/AnyPopup
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - AnyPopup
 - winuser/AnyPopup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - AnyPopup
---

# AnyPopup function


## -description

Indicates whether an owned, visible, top-level pop-up, or overlapped window exists on the screen. The function searches the entire screen, not just the calling application's client area.

This function is provided only for compatibility with 16-bit versions of Windows. It is generally not useful.



## -returns

Type: <b>BOOL</b>

If a pop-up window exists, the return value is nonzero, even if the pop-up window is completely covered by other windows.

If a pop-up window does not exist, the return value is zero.

## -remarks

This function does not detect unowned pop-up windows or windows that do not have the <b>WS_VISIBLE</b> style bit set.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getlastactivepopup">GetLastActivePopup</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showownedpopups">ShowOwnedPopups</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
