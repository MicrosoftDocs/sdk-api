---
UID: NF:prsht.PropSheet_SetNextText
title: PropSheet_SetNextText macro (prsht.h)
description: Sets the text of the Next button in a wizard. You can use this macro or send the PSM_SETNEXTTEXT message explicitly.
helpviewer_keywords: ["PropSheet_SetNextText","PropSheet_SetNextText macro [Windows Controls]","_shell_PropSheet_SetNextText","_shell_PropSheet_SetNextText_cpp","controls.PropSheet_SetNextText","controls._shell_PropSheet_SetNextText","prsht/PropSheet_SetNextText"]
old-location: controls\PropSheet_SetNextText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setnexttext.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetNextText, PropSheet_SetNextText macro [Windows Controls], _shell_PropSheet_SetNextText, _shell_PropSheet_SetNextText_cpp, controls.PropSheet_SetNextText, controls._shell_PropSheet_SetNextText, prsht/PropSheet_SetNextText
req.header: prsht.h
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
 - PropSheet_SetNextText
 - prsht/PropSheet_SetNextText
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
 - PropSheet_SetNextText
---

# PropSheet_SetNextText macro

## -syntax

```cpp
VOID PropSheet_SetNextText(
   HWND   hDlg,
   LPTSTR lpszText
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No meaningful return value.


## -description

Sets the text of the <b>Next</b> button in a wizard. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setnexttext">PSM_SETNEXTTEXT</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard.

### -param lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a buffer that contains the text.
