---
UID: NF:commctrl.Pager_GetButtonState
title: Pager_GetButtonState macro
author: windows-sdk-content
description: Retrieves the state of the specified button in a pager control. You can use this macro or send the PGM_GETBUTTONSTATE message explicitly.
old-location: controls\Pager_GetButtonState.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getbuttonstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Pager_GetButtonState, Pager_GetButtonState macro [Windows Controls], _win32_Pager_GetButtonState, _win32_Pager_GetButtonState_cpp, commctrl/Pager_GetButtonState, controls.Pager_GetButtonState, controls._win32_Pager_GetButtonState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Pager_GetButtonState macro


## -description


Retrieves the state of the specified button in a pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/58f99b67-fef7-4695-86e2-0579a2f6de2f">PGM_GETBUTTONSTATE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


### -param iButton

Type: <b>int</b>

Indicates which button to retrieve the state for. See the description for <i>iButton</i> in <a href="https://msdn.microsoft.com/58f99b67-fef7-4695-86e2-0579a2f6de2f">PGM_GETBUTTONSTATE</a> for a list of possible values. 

