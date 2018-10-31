---
UID: NF:windowsx.ComboBox_GetItemData
title: ComboBox_GetItemData macro
author: windows-sdk-content
description: Gets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the CB_GETITEMDATA message explicitly.
old-location: controls\ComboBox_GetItemData.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getitemdata.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ComboBox_GetItemData, ComboBox_GetItemData macro [Windows Controls], _win32_ComboBox_GetItemData, _win32_ComboBox_GetItemData_cpp, controls.ComboBox_GetItemData, controls._win32_ComboBox_GetItemData, windowsx/ComboBox_GetItemData
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
 - ComboBox_GetItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_GetItemData macro


## -description


Gets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/433b7f75-2831-4919-b931-c17ba651d145">CB_GETITEMDATA</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.

