---
UID: NF:windowsx.Edit_SetSel
title: Edit_SetSel macro
author: windows-sdk-content
description: Selects a range of characters in an edit or rich edit control. You can use this macro or send the EM_SETSEL message explicitly.
old-location: controls\Edit_SetSel.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setsel.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Edit_SetSel, Edit_SetSel macro [Windows Controls], _win32_Edit_SetSel, _win32_Edit_SetSel_cpp, controls.Edit_SetSel, controls._win32_Edit_SetSel, windowsx/Edit_SetSel
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
 - Edit_SetSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetSel macro


## -description


Selects a range of characters in an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761661(v=VS.85).aspx">EM_SETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param ichStart

Type: <b>int</b>

The starting character position of the selection. 


### -param ichEnd

Type: <b>int</b>

The ending character position of the selection. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761661(v=VS.85).aspx">EM_SETSEL</a>.



