---
UID: NF:windowsx.Button_SetText
title: Button_SetText macro (windowsx.h)
description: Sets the text of a button.helpviewer_keywords: ["Button_SetText","Button_SetText macro [Windows Controls]","_win32_Button_SetText","_win32_Button_SetText_cpp","controls.Button_SetText","controls._win32_Button_SetText","windowsx/Button_SetText"]
old-location: controls\Button_SetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_settext.htm
ms.date: 12/05/2018
ms.keywords: Button_SetText, Button_SetText macro [Windows Controls], _win32_Button_SetText, _win32_Button_SetText_cpp, controls.Button_SetText, controls._win32_Button_SetText, windowsx/Button_SetText
f1_keywords:
- windowsx/Button_SetText
dev_langs:
- c++
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
- Button_SetText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_SetText macro


## -description


Sets the text of a button.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.


### -param lpsz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a null-terminated string to be used as the button text.


## -remarks



The macro expands to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>.	



