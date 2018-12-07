---
UID: NF:windowsx.Button_SetStyle
title: Button_SetStyle macro
author: windows-sdk-content
description: Sets the style of a button. You can use this macro or send the BM_SETSTYLE message explicitly.
old-location: controls\Button_SetStyle.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setstyle.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Button_SetStyle, Button_SetStyle macro [Windows Controls], _win32_Button_SetStyle, _win32_Button_SetStyle_cpp, controls.Button_SetStyle, controls._win32_Button_SetStyle, windowsx/Button_SetStyle
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
 - Button_SetStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetStyle macro


## -description


Sets the style of a button. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761824(v=VS.85).aspx">BM_SETSTYLE</a> message explicitly. 



## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


### -param style

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The button style. This parameter can be a combination of button styles. For a table of button styles, see <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">Button Styles</a>. 


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to redraw the button; otherwise <b>FALSE</b>.

