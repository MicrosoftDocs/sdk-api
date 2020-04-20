---
UID: NF:windowsx.Edit_SetRect
title: Edit_SetRect macro (windowsx.h)
description: Sets the formatting rectangle of an edit control. You can use this macro or send the EM_SETRECT message explicitly.helpviewer_keywords: ["Edit_SetRect","Edit_SetRect macro [Windows Controls]","_win32_Edit_SetRect","_win32_Edit_SetRect_cpp","controls.Edit_SetRect","controls._win32_Edit_SetRect","windowsx/Edit_SetRect"]
old-location: controls\Edit_SetRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setrect.htm
ms.date: 12/05/2018
ms.keywords: Edit_SetRect, Edit_SetRect macro [Windows Controls], _win32_Edit_SetRect, _win32_Edit_SetRect_cpp, controls.Edit_SetRect, controls._win32_Edit_SetRect, windowsx/Edit_SetRect
f1_keywords:
- windowsx/Edit_SetRect
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
- Edit_SetRect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetRect macro


## -description


Sets the formatting rectangle of an edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setrect">EM_SETRECT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the new dimensions of the rectangle. If this parameter is <b>NULL</b>, the formatting rectangle is set to its default values. 


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setrect">EM_SETRECT</a>.



