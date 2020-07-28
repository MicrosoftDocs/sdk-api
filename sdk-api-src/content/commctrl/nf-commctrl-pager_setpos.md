---
UID: NF:commctrl.Pager_SetPos
title: Pager_SetPos macro (commctrl.h)
description: Sets the scroll position for the pager control. You can use this macro or send the PGM_SETPOS message explicitly.
helpviewer_keywords: ["Pager_SetPos","Pager_SetPos macro [Windows Controls]","_win32_Pager_SetPos","_win32_Pager_SetPos_cpp","commctrl/Pager_SetPos","controls.Pager_SetPos","controls._win32_Pager_SetPos"]
old-location: controls\Pager_SetPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setpos.htm
ms.date: 12/05/2018
ms.keywords: Pager_SetPos, Pager_SetPos macro [Windows Controls], _win32_Pager_SetPos, _win32_Pager_SetPos_cpp, commctrl/Pager_SetPos, controls.Pager_SetPos, controls._win32_Pager_SetPos
f1_keywords:
- commctrl/Pager_SetPos
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
- Pager_SetPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Pager_SetPos macro


## -description


Sets the scroll position for the pager control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/pgm-setpos">PGM_SETPOS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control. 


### -param iPos

Type: <b>int</b>

Value of type <b>int</b> that contains the new scroll position, in pixels. 

