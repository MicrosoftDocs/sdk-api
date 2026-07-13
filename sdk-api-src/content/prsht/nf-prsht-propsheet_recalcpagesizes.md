---
UID: NF:prsht.PropSheet_RecalcPageSizes
title: PropSheet_RecalcPageSizes macro (prsht.h)
description: Recalculates the page size of a standard or wizard property sheet after pages have been added or removed. You can use this macro or send the PSM_RECALCPAGESIZES message explicitly.
helpviewer_keywords: ["PropSheet_RecalcPageSizes","PropSheet_RecalcPageSizes macro [Windows Controls]","_win32_PropSheet_RecalcPageSizes","_win32_PropSheet_RecalcPageSizes_cpp","controls.PropSheet_RecalcPageSizes","controls._win32_PropSheet_RecalcPageSizes","prsht/PropSheet_RecalcPageSizes"]
old-location: controls\PropSheet_RecalcPageSizes.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_recalcpagesizes.htm
ms.date: 10/21/2024
ms.keywords: PropSheet_RecalcPageSizes, PropSheet_RecalcPageSizes macro [Windows Controls], _win32_PropSheet_RecalcPageSizes, _win32_PropSheet_RecalcPageSizes_cpp, controls.PropSheet_RecalcPageSizes, controls._win32_PropSheet_RecalcPageSizes, prsht/PropSheet_RecalcPageSizes
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
 - PropSheet_RecalcPageSizes
 - prsht/PropSheet_RecalcPageSizes
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
 - PropSheet_RecalcPageSizes
---

# PropSheet_RecalcPageSizes macro

## -syntax

```cpp
BOOL PropSheet_RecalcPageSizes(
   HWND hDlg
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Recalculates the page size of a standard or wizard property sheet after pages have been added or removed. You can use this macro or send the <a href="/windows/desktop/Controls/psm-recalcpagesizes">PSM_RECALCPAGESIZES</a> message explicitly.

## -parameters

### -param hDlg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet's dialog box.

## -remarks

When a property sheet is created, it is sized to fit its initial collection of pages. To maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed. With common controls <a href="/windows/desktop/Controls/common-control-versions">version 5.80</a> and later, applications should use the <b>PropSheet_RecalcPageSizes</b> macro after adding or removing pages with <a href="/windows/desktop/api/prsht/nf-prsht-propsheet_addpage">PropSheet_AddPage</a>, <a href="/windows/desktop/api/prsht/nf-prsht-propsheet_insertpage">PropSheet_InsertPage</a>, <a href="/windows/desktop/api/prsht/nf-prsht-propsheet_removepage">PropSheet_RemovePage</a>, or their equivalent messages. It ensures that the property sheet is properly sized for its current collection of pages. If this macro or the equivalent message is not used, some property sheet pages may be truncated or too large.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>
