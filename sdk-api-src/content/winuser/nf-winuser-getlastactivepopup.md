---
UID: NF:winuser.GetLastActivePopup
title: GetLastActivePopup function (winuser.h)
author: windows-sdk-content
description: Determines which pop-up window owned by the specified window was most recently active.
old-location: winmsg\getlastactivepopup.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getlastactivepopup.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLastActivePopup, GetLastActivePopup function [Windows and Messages], _win32_GetLastActivePopup, _win32_getlastactivepopup_cpp, winmsg.getlastactivepopup, winui._win32_getlastactivepopup, winuser/GetLastActivePopup
ms.topic: function
f1_keywords: ["winuser/GetLastActivePopup"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetLastActivePopup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetLastActivePopup function


## -description


Determines which pop-up window owned by the specified window was most recently active. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the owner window. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value identifies the most recently active pop-up window. The return value is the same as the <i>hWnd</i> parameter, if any of the following conditions are met: 

<ul>
<li>The window identified by hWnd was most recently active.</li>
<li>The window identified by hWnd does not own any pop-up windows.</li>
<li>The window identifies by hWnd is not a top-level window, or it is owned by another window.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-anypopup">AnyPopup</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showownedpopups">ShowOwnedPopups</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/windows">Windows</a>
 

 

