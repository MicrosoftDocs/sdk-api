---
UID: NF:prsht.PropSheet_SetFinishText
title: PropSheet_SetFinishText macro (prsht.h)
description: Sets the text of the Finish button in a wizard, shows and enables the button, and hides the Next and Back buttons. You can use this macro or send the PSM_SETFINISHTEXT message explicitly.
helpviewer_keywords: ["PropSheet_SetFinishText","PropSheet_SetFinishText macro [Windows Controls]","_win32_PropSheet_SetFinishText","_win32_PropSheet_SetFinishText_cpp","controls.PropSheet_SetFinishText","controls._win32_PropSheet_SetFinishText","prsht/PropSheet_SetFinishText"]
old-location: controls\PropSheet_SetFinishText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setfinishtext.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetFinishText, PropSheet_SetFinishText macro [Windows Controls], _win32_PropSheet_SetFinishText, _win32_PropSheet_SetFinishText_cpp, controls.PropSheet_SetFinishText, controls._win32_PropSheet_SetFinishText, prsht/PropSheet_SetFinishText
req.header: prsht.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PropSheet_SetFinishText
 - prsht/PropSheet_SetFinishText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_SetFinishText
---

# PropSheet_SetFinishText macro

## -syntax

```cpp
VOID PropSheet_SetFinishText(
   HWND   hDlg,
   LPTSTR lpszText
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Sets the text of the Finish button in a wizard, shows and enables the button, and hides the Next and Back buttons. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setfinishtext">PSM_SETFINISHTEXT</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Window handle (HWND) of the wizard property sheet.

### -param lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to the new text for the Finish button.

## -remarks

By default, the Finish button does not have a keyboard accelerator. You can create a keyboard accelerator with this macro by including an ampersand (&amp;) in the text string that you assign to <i>lpszText</i>. For example, "&amp;Finish" defines F as the accelerator key.
