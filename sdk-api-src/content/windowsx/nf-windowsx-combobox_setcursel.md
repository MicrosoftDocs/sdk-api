---
UID: NF:windowsx.ComboBox_SetCurSel
title: ComboBox_SetCurSel macro
author: windows-sdk-content
description: Sets the currently selected item in a combo box. You can use this macro or send the CB_SETCURSEL message explicitly.
old-location: controls\ComboBox_SetCurSel.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setcursel.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ComboBox_SetCurSel, ComboBox_SetCurSel macro [Windows Controls], _win32_ComboBox_SetCurSel, _win32_ComboBox_SetCurSel_cpp, controls.ComboBox_SetCurSel, controls._win32_ComboBox_SetCurSel, windowsx/ComboBox_SetCurSel
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
 - ComboBox_SetCurSel
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
- ComboBox_SetCurSel
: 
---

# ComboBox_SetCurSel macro


## -description


Sets the currently selected item in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775899(v=VS.85).aspx">CB_SETCURSEL</a> message explicitly.




## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to select, or –1 to clear the selection.

