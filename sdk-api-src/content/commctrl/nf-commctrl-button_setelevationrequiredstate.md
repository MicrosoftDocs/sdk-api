---
UID: NF:commctrl.Button_SetElevationRequiredState
title: Button_SetElevationRequiredState macro
author: windows-sdk-content
description: Sets the elevation required state for a specified button or command link to display an elevated icon. Use this macro or send the BCM_SETSHIELD message explicitly.
old-location: controls\Button_SetElevationRequiredState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setelevationrequiredstate.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Button_SetElevationRequiredState, Button_SetElevationRequiredState macro [Windows Controls], _shell_Button_SetElevationRequiredState, _shell_Button_SetElevationRequiredState_cpp, commctrl/Button_SetElevationRequiredState, controls.Button_SetElevationRequiredState, controls._shell_Button_SetElevationRequiredState
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Button_SetElevationRequiredState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Button_SetElevationRequiredState macro


## -description


Sets the elevation required state for a specified button or command link to display an elevated icon. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775979(v=VS.85).aspx">BCM_SETSHIELD</a> message explicitly. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the button control. 


### -param fRequired [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

<b>TRUE</b> to draw an elevated icon, or <b>FALSE</b> otherwise.


## -remarks



An application must use comctl32.dll version 6 to gain this functionality.



