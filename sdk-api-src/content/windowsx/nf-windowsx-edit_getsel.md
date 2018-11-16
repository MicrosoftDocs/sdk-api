---
UID: NF:windowsx.Edit_GetSel
title: Edit_GetSel macro
author: windows-sdk-content
description: Gets the starting and ending character positions of the current selection in an edit or rich edit control. You can use this macro or send the EM_GETSEL message explicitly.
old-location: controls\Edit_GetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getsel.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Edit_GetSel, Edit_GetSel macro [Windows Controls], _win32_Edit_GetSel, _win32_Edit_GetSel_cpp, controls.Edit_GetSel, controls._win32_Edit_GetSel, windowsx/Edit_GetSel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - Edit_GetSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- windowsx.h
: 
- Edit_GetSel
: 
---

# Edit_GetSel macro


## -description


Gets the starting and ending character positions of the current selection in an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761598(v=VS.85).aspx">EM_GETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



This macro does not have the complete functionality of the <a href="https://msdn.microsoft.com/en-us/library/Bb761598(v=VS.85).aspx">EM_GETSEL</a> message, because it does not receive the 32-bit return values in the parameters of <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>.



