---
UID: NF:commctrl.Button_SetDropDownState
title: Button_SetDropDownState macro (commctrl.h)
author: windows-sdk-content
description: Sets the drop down state for a specified button with style of BS_SPLITBUTTON. Use this macro or send the BCM_SETDROPDOWNSTATE message explicitly.
old-location: controls\Button_SetDropDownState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setdropdownstate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Button_SetDropDownState, Button_SetDropDownState macro [Windows Controls], _shell_Button_SetDropDownState, _shell_Button_SetDropDownState_cpp, commctrl/Button_SetDropDownState, controls.Button_SetDropDownState, controls._shell_Button_SetDropDownState
ms.topic: macro
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
 - Button_SetDropDownState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetDropDownState macro


## -description


Sets the drop down state for a specified button with style of <a href="https://msdn.microsoft.com/en-us/library/Bb775951(v=VS.85).aspx">BS_SPLITBUTTON</a>. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775973(v=VS.85).aspx">BCM_SETDROPDOWNSTATE</a> message explicitly. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control. 


### -param fDropDown [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> for state of  BST_DROPDOWNPUSHED, or <b>FALSE</b> otherwise.

