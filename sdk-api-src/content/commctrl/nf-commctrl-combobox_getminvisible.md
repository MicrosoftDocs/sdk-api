---
UID: NF:commctrl.ComboBox_GetMinVisible
title: ComboBox_GetMinVisible macro
author: windows-sdk-content
description: Gets the minimum number of visible items in the drop-down list of a combo box.
old-location: controls\ComboBox_GetMinVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getminvisible.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComboBox_GetMinVisible, ComboBox_GetMinVisible macro [Windows Controls], _win32_ComboBox_GetMinVisible, _win32_ComboBox_GetMinVisible_cpp, commctrl/ComboBox_GetMinVisible, controls.ComboBox_GetMinVisible, controls._win32_ComboBox_GetMinVisible
ms.topic: macro
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - ComboBox_GetMinVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_GetMinVisible macro


## -description


Gets the minimum number of visible items in the drop-down list of a combo box. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Specifies the combo box. 


## -remarks



When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar. 

To use <b>ComboBox_GetMinVisible</b>, the application must specify comctl32.dll version 6 in the manifest. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775869(v=VS.85).aspx">CB_GETMINVISIBLE</a>
 

 

