---
UID: NF:windowsx.ComboBox_InsertString
title: ComboBox_InsertString macro
author: windows-sdk-content
description: Adds a string to a list in a combo box at the specified location. You can use this macro or send the CB_INSERTSTRING message explicitly.
old-location: controls\ComboBox_InsertString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_insertstring.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ComboBox_InsertString, ComboBox_InsertString macro [Windows Controls], _win32_ComboBox_InsertString, _win32_ComboBox_InsertString_cpp, controls.ComboBox_InsertString, controls._win32_ComboBox_InsertString, windowsx/ComboBox_InsertString
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
 - ComboBox_InsertString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_InsertString macro


## -description


Adds a string to a list in a combo box at the specified location. You can use this macro or send the <a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index at which to insert the string, or –1 to add it to the end of the list. 


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The string to add.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a>.
	



