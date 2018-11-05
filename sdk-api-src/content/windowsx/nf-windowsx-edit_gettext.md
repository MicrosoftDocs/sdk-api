---
UID: NF:windowsx.Edit_GetText
title: Edit_GetText macro
author: windows-sdk-content
description: Gets the text of an edit control.
old-location: controls\edit_GetText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_gettext.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Edit_GetText, Edit_GetText macro [Windows Controls], _win32_edit_GetText, _win32_edit_GetText_cpp, controls._win32_edit_GetText, controls.edit_GetText, windowsx/Edit_GetText
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
 - Edit_GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetText macro


## -description


Gets the text of an edit control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control.


### -param lpch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to the buffer that will receive the text.


### -param cchMax

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the NULL terminator.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a>.
	



