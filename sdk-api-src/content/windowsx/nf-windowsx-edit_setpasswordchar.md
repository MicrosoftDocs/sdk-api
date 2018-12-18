---
UID: NF:windowsx.Edit_SetPasswordChar
title: Edit_SetPasswordChar macro
author: windows-sdk-content
description: Sets or removes the password character for an edit or rich edit control. When a password character is set, that character is displayed in place of the characters typed by the user. You can use this macro or send the EM_SETPASSWORDCHAR message explicitly.
old-location: controls\Edit_SetPasswordChar.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setpasswordchar.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Edit_SetPasswordChar, Edit_SetPasswordChar macro [Windows Controls], _win32_Edit_SetPasswordChar, _win32_Edit_SetPasswordChar_cpp, controls.Edit_SetPasswordChar, controls._win32_Edit_SetPasswordChar, windowsx/Edit_SetPasswordChar
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
 - Edit_SetPasswordChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetPasswordChar macro


## -description


Sets or removes the password character for an edit or rich edit control. When a password character is set, that character is displayed in place of the characters typed by the user. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761653(v=VS.85).aspx">EM_SETPASSWORDCHAR</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param ch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The character to be displayed in place of the characters typed by the user. If this parameter is zero, the control removes the current password character and displays the characters typed by the user. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761653(v=VS.85).aspx">EM_SETPASSWORDCHAR</a>.



