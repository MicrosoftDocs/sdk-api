---
UID: NF:windowsx.ComboBox_GetItemHeight
title: ComboBox_GetItemHeight macro (windowsx.h)
author: windows-sdk-content
description: Retrieves the height of list items in a combo box. You can use this macro or send the CB_GETITEMHEIGHT message explicitly.
old-location: controls\ComboBox_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getitemheight.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ComboBox_GetItemHeight, ComboBox_GetItemHeight macro [Windows Controls], _win32_ComboBox_GetItemHeight, _win32_ComboBox_GetItemHeight_cpp, controls.ComboBox_GetItemHeight, controls._win32_ComboBox_GetItemHeight, windowsx/ComboBox_GetItemHeight
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
 - ComboBox_GetItemHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_GetItemHeight macro


## -description


Retrieves the height of list items in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775860(v=VS.85).aspx">CB_GETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



This macro passes zero as the <i>wParam</i> member of <a href="https://msdn.microsoft.com/en-us/library/ms644950(v=VS.85).aspx">SendMessage</a>. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775860(v=VS.85).aspx">CB_GETITEMHEIGHT</a>.
	



