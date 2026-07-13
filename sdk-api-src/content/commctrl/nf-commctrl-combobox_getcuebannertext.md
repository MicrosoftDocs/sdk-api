---
UID: NF:commctrl.ComboBox_GetCueBannerText
title: ComboBox_GetCueBannerText macro (commctrl.h)
description: Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the CB_GETCUEBANNER message explicitly.
helpviewer_keywords: ["ComboBox_GetCueBannerText","ComboBox_GetCueBannerText macro [Windows Controls]","_shell_ComboBox_GetCueBannerText","_shell_ComboBox_GetCueBannerText_cpp","commctrl/ComboBox_GetCueBannerText","controls.ComboBox_GetCueBannerText","controls._shell_ComboBox_GetCueBannerText"]
old-location: controls\ComboBox_GetCueBannerText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getcuebannertext.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetCueBannerText, ComboBox_GetCueBannerText macro [Windows Controls], _shell_ComboBox_GetCueBannerText, _shell_ComboBox_GetCueBannerText_cpp, commctrl/ComboBox_GetCueBannerText, controls.ComboBox_GetCueBannerText, controls._shell_ComboBox_GetCueBannerText
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
 - ComboBox_GetCueBannerText
 - commctrl/ComboBox_GetCueBannerText
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
 - ComboBox_GetCueBannerText
---

# ComboBox_GetCueBannerText macro

## -syntax

```cpp
BOOL ComboBox_GetCueBannerText(
   HWND   hwnd,
   LPWSTR lpwText,
   int    cchText
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or an error value otherwise.


## -description

Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the <a href="/windows/desktop/Controls/cb-getcuebanner">CB_GETCUEBANNER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the combo box.

### -param lpwText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

A pointer to a Unicode string buffer that receives the cue banner text. The calling application is responsible for allocating the memory for the buffer. The buffer size must be equal to the length of the cue banner string in <b>WCHAR</b><b>s</b>, plus 1—for the terminating <b>NULL</b> <b>WCHAR</b>.

### -param cchText

Type: <b>int</b>

The size of the buffer pointed to by <i>lpwText</i> in <b>WCHAR</b><b>s</b>.

## -see-also

<a href="/windows/desktop/Controls/combo-box-features">Combo Box Features</a>
