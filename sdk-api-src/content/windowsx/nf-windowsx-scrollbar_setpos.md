---
UID: NF:windowsx.ScrollBar_SetPos
title: ScrollBar_SetPos macro (windowsx.h)
description: Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.
helpviewer_keywords: ["ScrollBar_SetPos","ScrollBar_SetPos macro [Windows Controls]","_win32_ScrollBar_SetPos","_win32_ScrollBar_SetPos_cpp","controls.ScrollBar_SetPos","controls._win32_ScrollBar_SetPos","windowsx/ScrollBar_SetPos"]
old-location: controls\ScrollBar_SetPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_setpos.htm
ms.date: 12/05/2018
ms.keywords: ScrollBar_SetPos, ScrollBar_SetPos macro [Windows Controls], _win32_ScrollBar_SetPos, _win32_ScrollBar_SetPos_cpp, controls.ScrollBar_SetPos, controls._win32_ScrollBar_SetPos, windowsx/ScrollBar_SetPos
f1_keywords:
- windowsx/ScrollBar_SetPos
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
- ScrollBar_SetPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ScrollBar_SetPos macro


## -description


Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box. 
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setscrollpos">SetScrollPos</a> function, which is deprecated. New applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setscrollinfo">SetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param pos

Type: <b>int</b>

The new position of the scroll box.


### -param fRedraw

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to redraw the control; otherwise <b>FALSE</b>.

