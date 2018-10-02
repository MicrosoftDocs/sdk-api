---
UID: NF:commctrl.Pager_ForwardMouse
title: Pager_ForwardMouse macro
author: windows-sdk-content
description: Enables or disables mouse forwarding for the pager control. When mouse forwarding is enabled, the pager control forwards WM_MOUSEMOVE messages to the contained window. You can use this macro or send the PGM_FORWARDMOUSE message explicitly.
old-location: controls\Pager_ForwardMouse.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_forwardmouse.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Pager_ForwardMouse, Pager_ForwardMouse macro [Windows Controls], _win32_Pager_ForwardMouse, _win32_Pager_ForwardMouse_cpp, commctrl/Pager_ForwardMouse, controls.Pager_ForwardMouse, controls._win32_Pager_ForwardMouse
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# Pager_ForwardMouse macro


## -description


Enables or disables mouse forwarding for the pager control. When mouse forwarding is enabled, the pager control forwards <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> messages to the contained window. You can use this macro or send the <a href="https://msdn.microsoft.com/269972fe-50b3-4c9f-b5ac-65e768b30684">PGM_FORWARDMOUSE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


### -param bForward

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>BOOL</b> value that determines if mouse forwarding is enabled or disabled. If this value is nonzero, mouse forwarding is enabled. If this value is zero, mouse forwarding is disabled. 

