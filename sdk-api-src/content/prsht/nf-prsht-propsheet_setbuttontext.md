---
UID: NF:prsht.PropSheet_SetButtonText
title: PropSheet_SetButtonText macro (prsht.h)
description: Sets the text of a button in an Aero wizard. You can use this macro or send the PSM_SETBUTTONTEXT message explicitly.
helpviewer_keywords: ["PSWIZB_BACK","PSWIZB_CANCEL","PSWIZB_FINISH","PSWIZB_NEXT","PropSheet_SetButtonText","PropSheet_SetButtonText macro [Windows Controls]","_win32_PropSheet_SetButtonText","_win32_PropSheet_SetButtonText_cpp","controls.PropSheet_SetButtonText","controls._win32_PropSheet_SetButtonText","prsht/PropSheet_SetButtonText"]
old-location: controls\PropSheet_SetButtonText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setbuttontext.htm
ms.date: 10/21/2024
ms.keywords: PSWIZB_BACK, PSWIZB_CANCEL, PSWIZB_FINISH, PSWIZB_NEXT, PropSheet_SetButtonText, PropSheet_SetButtonText macro [Windows Controls], _win32_PropSheet_SetButtonText, _win32_PropSheet_SetButtonText_cpp, controls.PropSheet_SetButtonText, controls._win32_PropSheet_SetButtonText, prsht/PropSheet_SetButtonText
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
 - PropSheet_SetButtonText
 - prsht/PropSheet_SetButtonText
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
 - PropSheet_SetButtonText
---

# PropSheet_SetButtonText macro

## -syntax

```cpp
VOID PropSheet_SetButtonText(
   HWND    hDlg,
   DWORD   dwButton,
   LPCTSTR lpszText
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Sets the text of a button in an Aero wizard. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setbuttontext">PSM_SETBUTTONTEXT</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard.

### -param dwButton

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One of the following values specifying the button whose text is set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_BACK"></a><a id="pswizb_back"></a><dl>
<dt><b>PSWIZB_BACK</b></dt>
</dl>
</td>
<td width="60%">
0x0001. The <b>Back</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_NEXT"></a><a id="pswizb_next"></a><dl>
<dt><b>PSWIZB_NEXT</b></dt>
</dl>
</td>
<td width="60%">
0x0002. The <b>Next</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_FINISH"></a><a id="pswizb_finish"></a><dl>
<dt><b>PSWIZB_FINISH</b></dt>
</dl>
</td>
<td width="60%">
0x0004. The <b>Finish</b> button.

</td>
</tr>
<tr>
<td width="40%"><a id="PSWIZB_CANCEL"></a><a id="pswizb_cancel"></a><dl>
<dt><b>PSWIZB_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
0x0010. The <b>Cancel</b> button.

</td>
</tr>
</table>

### -param lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The text to set.
