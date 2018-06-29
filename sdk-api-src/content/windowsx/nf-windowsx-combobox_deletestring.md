---
UID: NF:windowsx.ComboBox_DeleteString
title: ComboBox_DeleteString macro
author: windows-sdk-content
description: Deletes the item at the specified location in a list in a combo box. You can use this macro or send the CB_DELETESTRING message explicitly.
old-location: controls\ComboBox_DeleteString.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_deletestring.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ComboBox_DeleteString, ComboBox_DeleteString macro [Windows Controls], _win32_ComboBox_DeleteString, _win32_ComboBox_DeleteString_cpp, controls.ComboBox_DeleteString, controls._win32_ComboBox_DeleteString, windowsx/ComboBox_DeleteString
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ComboBox_DeleteString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_DeleteString macro


## -description


Deletes the item at the specified location in a list in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775830(v=VS.85).aspx">CB_DELETESTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to delete.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/Bb775830(v=VS.85).aspx">CB_DELETESTRING</a>




