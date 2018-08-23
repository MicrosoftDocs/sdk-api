---
UID: NF:winuser.AnyPopup
title: AnyPopup function
author: windows-sdk-content
description: Indicates whether an owned, visible, top-level pop-up, or overlapped window exists on the screen. The function searches the entire screen, not just the calling application's client area.
old-location: winmsg\anypopup.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\anypopup.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: AnyPopup, AnyPopup function [Windows and Messages], _win32_AnyPopup, _win32_anypopup_cpp, winmsg.anypopup, winui._win32_anypopup, winuser/AnyPopup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - AnyPopup
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# AnyPopup function


## -description


Indicates whether an owned, visible, top-level pop-up, or overlapped window exists on the screen. The function searches the entire screen, not just the calling application's client area.

This function is provided only for compatibility with 16-bit versions of Windows. It is generally not useful.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If a pop-up window exists, the return value is nonzero, even if the pop-up window is completely covered by other windows.

If a pop-up window does not exist, the return value is zero. 




## -remarks



This function does not detect unowned pop-up windows or windows that do not have the <b>WS_VISIBLE</b> style bit set. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633507(v=VS.85).aspx">GetLastActivePopup</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633547(v=VS.85).aspx">ShowOwnedPopups</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

