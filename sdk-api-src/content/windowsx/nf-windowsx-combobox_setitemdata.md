---
UID: NF:windowsx.ComboBox_SetItemData
title: ComboBox_SetItemData macro
author: windows-driver-content
description: Sets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the CB_SETITEMDATA message explicitly.
old-location: controls\ComboBox_SetItemData.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setitemdata.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ComboBox_SetItemData, ComboBox_SetItemData macro [Windows Controls], _win32_ComboBox_SetItemData, _win32_ComboBox_SetItemData_cpp, controls.ComboBox_SetItemData, controls._win32_ComboBox_SetItemData, windowsx/ComboBox_SetItemData
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	ComboBox_SetItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_SetItemData macro


## -description


Sets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/8be9eb57-a635-4c52-9838-556368813c74">CB_SETITEMDATA</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The item data to set.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/8be9eb57-a635-4c52-9838-556368813c74">CB_SETITEMDATA</a>.
	



