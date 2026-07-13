---
UID: NF:commctrl.ComboBox_SetCueBannerText
title: ComboBox_SetCueBannerText macro (commctrl.h)
description: Sets the cue banner text that is displayed for the edit control of a combo box.
helpviewer_keywords: ["ComboBox_SetCueBannerText","ComboBox_SetCueBannerText macro [Windows Controls]","_shell_ComboBox_SetCueBannerText","_shell_ComboBox_SetCueBannerText_cpp","commctrl/ComboBox_SetCueBannerText","controls.ComboBox_SetCueBannerText","controls._shell_ComboBox_SetCueBannerText"]
old-location: controls\ComboBox_SetCueBannerText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setcuebannertext.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_SetCueBannerText, ComboBox_SetCueBannerText macro [Windows Controls], _shell_ComboBox_SetCueBannerText, _shell_ComboBox_SetCueBannerText_cpp, commctrl/ComboBox_SetCueBannerText, controls.ComboBox_SetCueBannerText, controls._shell_ComboBox_SetCueBannerText
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ComboBox_SetCueBannerText
 - commctrl/ComboBox_SetCueBannerText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ComboBox_SetCueBannerText
---

# ComboBox_SetCueBannerText macro

## -syntax

```cpp
BOOL ComboBox_SetCueBannerText(
   HWND    hwnd,
   LPCWSTR lpcwText
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or an error value otherwise.


## -description

Sets the cue banner text that is displayed for the edit control of a combo box.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the combo box.

### -param lpcwText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A pointer to a null-terminated Unicode string buffer that contains the text.

## -remarks

The cue banner is text that is displayed in the edit control of a combo box when there is no selection.

## -see-also

<a href="/windows/desktop/Controls/combo-box-features">Combo Box Features</a>
