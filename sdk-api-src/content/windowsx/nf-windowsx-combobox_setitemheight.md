---
UID: NF:windowsx.ComboBox_SetItemHeight
title: ComboBox_SetItemHeight macro
author: windows-sdk-content
description: Sets the height of list items or the selection field in a combo box. You can use this macro or send the CB_SETITEMHEIGHT message explicitly.
old-location: controls\ComboBox_SetItemHeight.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setitemheight.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ComboBox_SetItemHeight, ComboBox_SetItemHeight macro [Windows Controls], _win32_ComboBox_SetItemHeight, _win32_ComboBox_SetItemHeight_cpp, controls.ComboBox_SetItemHeight, controls._win32_ComboBox_SetItemHeight, windowsx/ComboBox_SetItemHeight
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
 - ComboBox_SetItemHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_SetItemHeight macro


## -description


Sets the height of list items or the selection field in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775911(v=VS.85).aspx">CB_SETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The component of the combo box for which to set the height. This parameter must be –1 to set the height of the selection field. It must be zero to set the height of list items, unless the combo box has the <a href="https://msdn.microsoft.com/en-us/library/Bb775796(v=VS.85).aspx">CBS_OWNERDRAWVARIABLE</a> style. In that case, the <i>index</i> parameter is the zero-based index of a specific list item.


### -param cyItem

Type: <b>int</b>

The height in pixels.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775911(v=VS.85).aspx">CB_SETITEMHEIGHT</a>.
	



