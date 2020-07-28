---
UID: NF:commctrl.Button_SetElevationRequiredState
title: Button_SetElevationRequiredState macro (commctrl.h)
description: Sets the elevation required state for a specified button or command link to display an elevated icon. Use this macro or send the BCM_SETSHIELD message explicitly.
helpviewer_keywords: ["Button_SetElevationRequiredState","Button_SetElevationRequiredState macro [Windows Controls]","_shell_Button_SetElevationRequiredState","_shell_Button_SetElevationRequiredState_cpp","commctrl/Button_SetElevationRequiredState","controls.Button_SetElevationRequiredState","controls._shell_Button_SetElevationRequiredState"]
old-location: controls\Button_SetElevationRequiredState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setelevationrequiredstate.htm
ms.date: 12/05/2018
ms.keywords: Button_SetElevationRequiredState, Button_SetElevationRequiredState macro [Windows Controls], _shell_Button_SetElevationRequiredState, _shell_Button_SetElevationRequiredState_cpp, commctrl/Button_SetElevationRequiredState, controls.Button_SetElevationRequiredState, controls._shell_Button_SetElevationRequiredState
f1_keywords:
- commctrl/Button_SetElevationRequiredState
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Button_SetElevationRequiredState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_SetElevationRequiredState macro


## -description


Sets the elevation required state for a specified button or command link to display an elevated icon. Use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/bcm-setshield">BCM_SETSHIELD</a> message explicitly. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control. 


### -param fRequired [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to draw an elevated icon, or <b>FALSE</b> otherwise.


## -remarks



An application must use comctl32.dll version 6 to gain this functionality.



