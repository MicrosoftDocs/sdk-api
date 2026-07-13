---
UID: NF:prsht.PropSheet_SetHeaderSubTitle
title: PropSheet_SetHeaderSubTitle macro (prsht.h)
description: Sets the subtitle text for the header of a wizard's interior page. You can use this macro or send the PSM_SETHEADERSUBTITLE message explicitly.
helpviewer_keywords: ["PropSheet_SetHeaderSubTitle","PropSheet_SetHeaderSubTitle macro [Windows Controls]","_win32_PropSheet_SetHeaderSubTitle","_win32_PropSheet_SetHeaderSubTitle_cpp","controls.PropSheet_SetHeaderSubTitle","controls._win32_PropSheet_SetHeaderSubTitle","prsht/PropSheet_SetHeaderSubTitle"]
old-location: controls\PropSheet_SetHeaderSubTitle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setheadersubtitle.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_SetHeaderSubTitle, PropSheet_SetHeaderSubTitle macro [Windows Controls], _win32_PropSheet_SetHeaderSubTitle, _win32_PropSheet_SetHeaderSubTitle_cpp, controls.PropSheet_SetHeaderSubTitle, controls._win32_PropSheet_SetHeaderSubTitle, prsht/PropSheet_SetHeaderSubTitle
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
 - PropSheet_SetHeaderSubTitle
 - prsht/PropSheet_SetHeaderSubTitle
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
 - PropSheet_SetHeaderSubTitle
---

# PropSheet_SetHeaderSubTitle macro

## -syntax

```cpp
VOID PropSheet_SetHeaderSubTitle(
   HWND   hDlg,
   int    index,
   LPCSTR lpszText
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

No return value.


## -description

Sets the subtitle text for the header of a wizard's interior page. You can use this macro or send the <a href="/windows/desktop/Controls/psm-setheadersubtitle">PSM_SETHEADERSUBTITLE</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the wizard's window.

### -param index

Type: <b>int</b>

Zero-based index of the page.

### -param lpszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

New header subtitle.

## -remarks

If you specify the current page, it will immediately be repainted to display the new subtitle.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_hwndtoindex">PropSheet_HwndToIndex</a>



<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_idtoindex">PropSheet_IdToIndex</a>



<a href="/windows/desktop/api/prsht/nf-prsht-propsheet_pagetoindex">PropSheet_PageToIndex</a>



<b>Reference</b>
