---
UID: NF:windowsx.ComboBox_GetDroppedControlRect
title: ComboBox_GetDroppedControlRect macro
author: windows-sdk-content
description: Retrieves the screen coordinates of a combo box in its dropped-down state. You can use this macro or send the CB_GETDROPPEDCONTROLRECT message explicitly.
old-location: controls\ComboBox_GetDroppedControlRect.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getdroppedcontrolrect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ComboBox_GetDroppedControlRect, ComboBox_GetDroppedControlRect macro [Windows Controls], _win32_ComboBox_GetDroppedControlRect, _win32_ComboBox_GetDroppedControlRect_cpp, controls.ComboBox_GetDroppedControlRect, controls._win32_ComboBox_GetDroppedControlRect, windowsx/ComboBox_GetDroppedControlRect
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
 - ComboBox_GetDroppedControlRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_GetDroppedControlRect macro


## -description


Retrieves the screen coordinates of a combo box in its dropped-down state. You can use this macro or send the <a href="https://msdn.microsoft.com/fd8d78c0-e1a8-49c8-9e35-a105d00b863c">CB_GETDROPPEDCONTROLRECT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the coordinates of the combo box in its dropped-down state.

