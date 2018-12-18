---
UID: NF:windowsx.ComboBox_SetExtendedUI
title: ComboBox_SetExtendedUI macro
author: windows-sdk-content
description: Selects either the default user interface (UI) or the extended UI for a combo box that has the CBS_DROPDOWN or CBS_DROPDOWNLIST style. You can use this macro or send the CB_SETEXTENDEDUI message explicitly.
old-location: controls\ComboBox_SetExtendedUI.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setextendedui.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComboBox_SetExtendedUI, ComboBox_SetExtendedUI macro [Windows Controls], _win32_ComboBox_SetExtendedUI, _win32_ComboBox_SetExtendedUI_cpp, controls.ComboBox_SetExtendedUI, controls._win32_ComboBox_SetExtendedUI, windowsx/ComboBox_SetExtendedUI
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
 - ComboBox_SetExtendedUI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_SetExtendedUI macro


## -description


Selects either the default user interface (UI) or the extended UI for a combo box that has the <a href="https://msdn.microsoft.com/en-us/library/Bb775796(v=VS.85).aspx">CBS_DROPDOWN</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb775796(v=VS.85).aspx">CBS_DROPDOWNLIST</a> style. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775905(v=VS.85).aspx">CB_SETEXTENDEDUI</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero to use the default UI, or nonzero to use the extended UI.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775905(v=VS.85).aspx">CB_SETEXTENDEDUI</a>.
	



