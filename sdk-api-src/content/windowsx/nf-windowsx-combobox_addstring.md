---
UID: NF:windowsx.ComboBox_AddString
title: ComboBox_AddString macro
author: windows-sdk-content
description: Adds a string to a list in a combo box.
old-location: controls\ComboBox_AddString.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_addstring.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ComboBox_AddString, ComboBox_AddString macro [Windows Controls], _win32_ComboBox_AddString, _win32_ComboBox_AddString_cpp, controls.ComboBox_AddString, controls._win32_ComboBox_AddString, windowsx/ComboBox_AddString
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
 - ComboBox_AddString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_AddString macro


## -description


Adds a string to a list in a combo box. If the combo box does not have the <a href="https://msdn.microsoft.com/library/Bb775796(v=VS.85).aspx">CBS_SORT</a> style, the string is added to the end of the list. Otherwise, the string is inserted into the list and the list is sorted. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775828(v=VS.85).aspx">CB_ADDSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The string to add.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/Bb775828(v=VS.85).aspx">CB_ADDSTRING</a>.
	



