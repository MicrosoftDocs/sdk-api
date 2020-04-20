---
UID: NF:prsht.PropSheet_UnChanged
title: PropSheet_UnChanged macro (prsht.h)
description: Informs a property sheet that information in a page has reverted to the previously saved state. You can use this macro or send the PSM_UNCHANGED message explicitly.helpviewer_keywords: ["PropSheet_UnChanged","PropSheet_UnChanged macro [Windows Controls]","_win32_PropSheet_UnChanged","_win32_PropSheet_UnChanged_cpp","controls.PropSheet_UnChanged","controls._win32_PropSheet_UnChanged","prsht/PropSheet_UnChanged"]
old-location: controls\PropSheet_UnChanged.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_unchanged.htm
ms.date: 12/05/2018
ms.keywords: PropSheet_UnChanged, PropSheet_UnChanged macro [Windows Controls], _win32_PropSheet_UnChanged, _win32_PropSheet_UnChanged_cpp, controls.PropSheet_UnChanged, controls._win32_PropSheet_UnChanged, prsht/PropSheet_UnChanged
f1_keywords:
- prsht/PropSheet_UnChanged
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Prsht.h
api_name:
- PropSheet_UnChanged
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_UnChanged macro


## -description


Informs a property sheet that information in a page has reverted to the previously saved state. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-unchanged">PSM_UNCHANGED</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the page that has reverted to the previously saved state.


## -remarks



The property sheet disables the <b>Apply Now</b> button if no other pages have registered changes with the property sheet.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>


