---
UID: NF:windowsx.Edit_SetModify
title: Edit_SetModify macro (windowsx.h)
description: Sets or clears the modification flag for an edit control. The modification flag indicates whether the text within the edit control has been modified. You can use this macro or send the EM_SETMODIFY message explicitly.helpviewer_keywords: ["Edit_SetModify","Edit_SetModify macro [Windows Controls]","_win32_Edit_SetModify","_win32_Edit_SetModify_cpp","controls.Edit_SetModify","controls._win32_Edit_SetModify","windowsx/Edit_SetModify"]
old-location: controls\Edit_SetModify.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setmodify.htm
ms.date: 12/05/2018
ms.keywords: Edit_SetModify, Edit_SetModify macro [Windows Controls], _win32_Edit_SetModify, _win32_Edit_SetModify_cpp, controls.Edit_SetModify, controls._win32_Edit_SetModify, windowsx/Edit_SetModify
f1_keywords:
- windowsx/Edit_SetModify
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
- Edit_SetModify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetModify macro


## -description


Sets or clears the modification flag for an edit control. The modification flag indicates whether the text within the edit control has been modified. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setmodify">EM_SETMODIFY</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param fModified

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the text has been modified; otherwise <b>FALSE</b>.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setmodify">EM_SETMODIFY</a>.



