---
UID: NF:windowsx.Edit_SetSel
title: Edit_SetSel macro (windowsx.h)
description: Selects a range of characters in an edit or rich edit control. You can use this macro or send the EM_SETSEL message explicitly.helpviewer_keywords: ["Edit_SetSel","Edit_SetSel macro [Windows Controls]","_win32_Edit_SetSel","_win32_Edit_SetSel_cpp","controls.Edit_SetSel","controls._win32_Edit_SetSel","windowsx/Edit_SetSel"]
old-location: controls\Edit_SetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setsel.htm
ms.date: 12/05/2018
ms.keywords: Edit_SetSel, Edit_SetSel macro [Windows Controls], _win32_Edit_SetSel, _win32_Edit_SetSel_cpp, controls.Edit_SetSel, controls._win32_Edit_SetSel, windowsx/Edit_SetSel
f1_keywords:
- windowsx/Edit_SetSel
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
- Edit_SetSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetSel macro


## -description


Selects a range of characters in an edit or rich edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setsel">EM_SETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param ichStart

Type: <b>int</b>

The starting character position of the selection. 


### -param ichEnd

Type: <b>int</b>

The ending character position of the selection. 


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setsel">EM_SETSEL</a>.



