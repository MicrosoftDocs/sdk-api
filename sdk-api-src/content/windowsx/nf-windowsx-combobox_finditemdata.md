---
UID: NF:windowsx.ComboBox_FindItemData
title: ComboBox_FindItemData macro
author: windows-sdk-content
description: Finds the first item in a combo box list that has the specified item data. You can use this macro or send the CB_FINDSTRING message explicitly.
old-location: controls\ComboBox_FindItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_finditemdata.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ComboBox_FindItemData, ComboBox_FindItemData macro [Windows Controls], _win32_ComboBox_FindItemData, _win32_ComboBox_FindItemData_cpp, controls.ComboBox_FindItemData, controls._win32_ComboBox_FindItemData, windowsx/ComboBox_FindItemData
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
 - ComboBox_FindItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_FindItemData macro


## -description


Finds the first item in a combo box list that has the specified item data. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775835(v=VS.85).aspx">CB_FINDSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire listis searched from the beginning.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The data to find.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775835(v=VS.85).aspx">CB_FINDSTRING</a>.
	



