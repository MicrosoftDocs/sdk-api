---
UID: NF:windowsx.Button_SetState
title: Button_SetState macro
author: windows-sdk-content
description: Sets the highlight state of a button. The highlight state indicates whether the button is highlighted as if the user had pushed it. You can use this macro or send the BM_SETSTATE message explicitly.
old-location: controls\Button_SetState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setstate.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: Button_SetState, Button_SetState macro [Windows Controls], _win32_Button_SetState, _win32_Button_SetState_cpp, controls.Button_SetState, controls._win32_Button_SetState, windowsx/Button_SetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: windowsx.h
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
 - Windowsx.h
api_name:
 - Button_SetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetState macro


## -description


Sets the highlight state of a button. The highlight state indicates whether the button is highlighted as if the user had pushed it. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761823(v=VS.85).aspx">BM_SETSTATE</a> message explicitly. 



## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param state

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to highlight the button; otherwise <b>FALSE</b>.


## -remarks



Highlighting  affects only the appearance of a button. It has no effect on the check state of a radio button or check box. 

A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button. The highlighting is removed when the user releases the mouse button. 



