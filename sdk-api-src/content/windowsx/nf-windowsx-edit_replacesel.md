---
UID: NF:windowsx.Edit_ReplaceSel
title: Edit_ReplaceSel macro (windowsx.h)
description: Replaces the selected text in an edit control or a rich edit control with the specified text. You can use this macro or send the EM_REPLACESEL message explicitly.helpviewer_keywords: ["Edit_ReplaceSel","Edit_ReplaceSel macro [Windows Controls]","_win32_Edit_ReplaceSel","_win32_Edit_ReplaceSel_cpp","controls.Edit_ReplaceSel","controls._win32_Edit_ReplaceSel","windowsx/Edit_ReplaceSel"]
old-location: controls\Edit_ReplaceSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_replacesel.htm
ms.date: 12/05/2018
ms.keywords: Edit_ReplaceSel, Edit_ReplaceSel macro [Windows Controls], _win32_Edit_ReplaceSel, _win32_Edit_ReplaceSel_cpp, controls.Edit_ReplaceSel, controls._win32_Edit_ReplaceSel, windowsx/Edit_ReplaceSel
f1_keywords:
- windowsx/Edit_ReplaceSel
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
- Edit_ReplaceSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_ReplaceSel macro


## -description


Replaces the selected text in an edit control or a rich edit control with the specified text. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-replacesel">EM_REPLACESEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param lpszReplace

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to a null-terminated string containing the replacement text.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-replacesel">EM_REPLACESEL</a>.



