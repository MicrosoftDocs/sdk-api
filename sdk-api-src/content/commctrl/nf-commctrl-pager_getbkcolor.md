---
UID: NF:commctrl.Pager_GetBkColor
title: Pager_GetBkColor macro (commctrl.h)
description: Retrieves the current background color for the pager control. You can use this macro or send the PGM_GETBKCOLOR message explicitly.
helpviewer_keywords: ["Pager_GetBkColor","Pager_GetBkColor macro [Windows Controls]","_win32_Pager_GetBkColor","_win32_Pager_GetBkColor_cpp","commctrl/Pager_GetBkColor","controls.Pager_GetBkColor","controls._win32_Pager_GetBkColor"]
old-location: controls\Pager_GetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getbkcolor.htm
ms.date: 12/05/2018
ms.keywords: Pager_GetBkColor, Pager_GetBkColor macro [Windows Controls], _win32_Pager_GetBkColor, _win32_Pager_GetBkColor_cpp, commctrl/Pager_GetBkColor, controls.Pager_GetBkColor, controls._win32_Pager_GetBkColor
f1_keywords:
- commctrl/Pager_GetBkColor
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
- Pager_GetBkColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Pager_GetBkColor macro


## -description


Retrieves the current background color for the pager control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/pgm-getbkcolor">PGM_GETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control. 


## -remarks



By default, the pager control will use the system button face color as the background color. This is the same color that can be retrieved by calling <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a> with COLOR_BTNFACE. 



