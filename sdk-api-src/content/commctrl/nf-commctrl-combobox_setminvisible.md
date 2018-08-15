---
UID: NF:commctrl.ComboBox_SetMinVisible
title: ComboBox_SetMinVisible macro
author: windows-sdk-content
description: Sets the minimum number of visible items in the drop-down list of a combo box.
old-location: controls\ComboBox_SetMinVisible.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setminvisible.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ComboBox_SetMinVisible, ComboBox_SetMinVisible macro [Windows Controls], _win32_ComboBox_SetMinVisible, _win32_ComboBox_SetMinVisible_cpp, commctrl/ComboBox_SetMinVisible, controls.ComboBox_SetMinVisible, controls._win32_ComboBox_SetMinVisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ComboBox_SetMinVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ComboBox_SetMinVisible macro


## -description


Sets the minimum number of visible items in the drop-down list of a combo box. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The combo box. 


### -param iMinVisible

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The minimum number of visible items. 


## -remarks



When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar. By default, 30 is the minimum number of visible items.

<code>Combobox_SetMinVisible (hwnd, iMinVisible)</code>

is equivalent to the following call.

<code>SendMessage((hwnd), CB_SETMINVISIBLE, (WPARAM) iMinVisible, 0);</code>

To use <b>ComboBox_SetMinVisible</b>, the application must specify comctl32.dll version 6 in the manifest. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775915(v=VS.85).aspx">CB_SETMINVISIBLE</a>
 

 

