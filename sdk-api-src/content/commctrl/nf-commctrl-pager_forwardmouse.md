---
UID: NF:commctrl.Pager_ForwardMouse
title: Pager_ForwardMouse macro (commctrl.h)
author: windows-sdk-content
description: Enables or disables mouse forwarding for the pager control. When mouse forwarding is enabled, the pager control forwards WM_MOUSEMOVE messages to the contained window. You can use this macro or send the PGM_FORWARDMOUSE message explicitly.
old-location: controls\Pager_ForwardMouse.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_forwardmouse.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Pager_ForwardMouse, Pager_ForwardMouse macro [Windows Controls], _win32_Pager_ForwardMouse, _win32_Pager_ForwardMouse_cpp, commctrl/Pager_ForwardMouse, controls.Pager_ForwardMouse, controls._win32_Pager_ForwardMouse
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Pager_ForwardMouse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Pager_ForwardMouse macro


## -description


Enables or disables mouse forwarding for the pager control. When mouse forwarding is enabled, the pager control forwards <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-mousemove">WM_MOUSEMOVE</a> messages to the contained window. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/pgm-forwardmouse">PGM_FORWARDMOUSE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control. 


### -param bForward

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>BOOL</b> value that determines if mouse forwarding is enabled or disabled. If this value is nonzero, mouse forwarding is enabled. If this value is zero, mouse forwarding is disabled. 

