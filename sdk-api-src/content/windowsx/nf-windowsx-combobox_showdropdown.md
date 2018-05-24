---
UID: NF:windowsx.ComboBox_ShowDropdown
title: ComboBox_ShowDropdown macro
author: windows-driver-content
description: Shows or hides the list in a combo box. You can use this macro or send the CB_SHOWDROPDOWN message explicitly.
old-location: controls\ComboBox_ShowDropdown.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_showdropdown.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ComboBox_ShowDropdown, ComboBox_ShowDropdown macro [Windows Controls], _win32_ComboBox_ShowDropdown, _win32_ComboBox_ShowDropdown_cpp, controls.ComboBox_ShowDropdown, controls._win32_ComboBox_ShowDropdown, windowsx/ComboBox_ShowDropdown
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
-	ComboBox_ShowDropdown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_ShowDropdown macro


## -description


Shows or hides the list in a combo box. You can use this macro or send the <a href="https://msdn.microsoft.com/32b995d7-eed6-4173-8525-0d356dea39b3">CB_SHOWDROPDOWN</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fShow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to show the dropdown, or <b>FALSE</b> to hide it.


## -remarks



This macro has no effect on a combo box created with the <a href="Combo_Box_Styles.htm">CBS_SIMPLE</a> style.
	



