---
UID: NF:commctrl.ComboBox_SetMinVisible
title: ComboBox_SetMinVisible macro (commctrl.h)
description: Sets the minimum number of visible items in the drop-down list of a combo box.
helpviewer_keywords: ["ComboBox_SetMinVisible","ComboBox_SetMinVisible macro [Windows Controls]","_win32_ComboBox_SetMinVisible","_win32_ComboBox_SetMinVisible_cpp","commctrl/ComboBox_SetMinVisible","controls.ComboBox_SetMinVisible","controls._win32_ComboBox_SetMinVisible"]
old-location: controls\ComboBox_SetMinVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setminvisible.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_SetMinVisible, ComboBox_SetMinVisible macro [Windows Controls], _win32_ComboBox_SetMinVisible, _win32_ComboBox_SetMinVisible_cpp, commctrl/ComboBox_SetMinVisible, controls.ComboBox_SetMinVisible, controls._win32_ComboBox_SetMinVisible
f1_keywords:
- commctrl/ComboBox_SetMinVisible
dev_langs:
- c++
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
- ComboBox_SetMinVisible
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_SetMinVisible macro


## -description


Sets the minimum number of visible items in the drop-down list of a combo box. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The combo box. 


### -param iMinVisible

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

The minimum number of visible items. 


## -remarks



When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar. By default, 30 is the minimum number of visible items.

<code>Combobox_SetMinVisible (hwnd, iMinVisible)</code>

is equivalent to the following call.

<code>SendMessage((hwnd), CB_SETMINVISIBLE, (WPARAM) iMinVisible, 0);</code>

To use <b>ComboBox_SetMinVisible</b>, the application must specify comctl32.dll version 6 in the manifest. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/cb-setminvisible">CB_SETMINVISIBLE</a>
 

 

