---
UID: NF:commctrl.ListView_SetBkColor
title: ListView_SetBkColor macro (commctrl.h)
description: Sets the background color of a list-view control. You can use this macro or send the LVM_SETBKCOLOR message explicitly.
helpviewer_keywords: ["ListView_SetBkColor","ListView_SetBkColor macro [Windows Controls]","_win32_ListView_SetBkColor","_win32_ListView_SetBkColor_cpp","commctrl/ListView_SetBkColor","controls.ListView_SetBkColor","controls._win32_ListView_SetBkColor"]
old-location: controls\ListView_SetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setbkcolor.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetBkColor, ListView_SetBkColor macro [Windows Controls], _win32_ListView_SetBkColor, _win32_ListView_SetBkColor_cpp, commctrl/ListView_SetBkColor, controls.ListView_SetBkColor, controls._win32_ListView_SetBkColor
f1_keywords:
- commctrl/ListView_SetBkColor
dev_langs:
- c++
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
- ListView_SetBkColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetBkColor macro


## -description


Sets the background color of a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setbkcolor">LVM_SETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param clrBk

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The background color to set or the CLR_NONE value for no background color. List-view controls with background colors redraw themselves significantly faster than those without background colors. 

