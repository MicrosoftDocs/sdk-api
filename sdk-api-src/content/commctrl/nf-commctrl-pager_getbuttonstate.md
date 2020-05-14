---
UID: NF:commctrl.Pager_GetButtonState
title: Pager_GetButtonState macro (commctrl.h)
description: Retrieves the state of the specified button in a pager control. You can use this macro or send the PGM_GETBUTTONSTATE message explicitly.helpviewer_keywords: ["Pager_GetButtonState","Pager_GetButtonState macro [Windows Controls]","_win32_Pager_GetButtonState","_win32_Pager_GetButtonState_cpp","commctrl/Pager_GetButtonState","controls.Pager_GetButtonState","controls._win32_Pager_GetButtonState"]
old-location: controls\Pager_GetButtonState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getbuttonstate.htm
ms.date: 12/05/2018
ms.keywords: Pager_GetButtonState, Pager_GetButtonState macro [Windows Controls], _win32_Pager_GetButtonState, _win32_Pager_GetButtonState_cpp, commctrl/Pager_GetButtonState, controls.Pager_GetButtonState, controls._win32_Pager_GetButtonState
f1_keywords:
- commctrl/Pager_GetButtonState
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
- Pager_GetButtonState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Pager_GetButtonState macro


## -description


Retrieves the state of the specified button in a pager control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/pgm-getbuttonstate">PGM_GETBUTTONSTATE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control. 


### -param iButton

Type: <b>int</b>

Indicates which button to retrieve the state for. See the description for <i>iButton</i> in <a href="https://docs.microsoft.com/windows/desktop/Controls/pgm-getbuttonstate">PGM_GETBUTTONSTATE</a> for a list of possible values. 

