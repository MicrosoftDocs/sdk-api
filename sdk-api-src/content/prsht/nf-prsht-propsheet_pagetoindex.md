---
UID: NF:prsht.PropSheet_PageToIndex
title: PropSheet_PageToIndex macro (prsht.h)
description: Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_PAGETOINDEX message explicitly.
helpviewer_keywords: ["PropSheet_PageToIndex","PropSheet_PageToIndex macro [Windows Controls]","_win32_PropSheet_PageToIndex","_win32_PropSheet_PageToIndex_cpp","controls.PropSheet_PageToIndex","controls._win32_PropSheet_PageToIndex","prsht/PropSheet_PageToIndex"]
old-location: controls\PropSheet_PageToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_pagetoindex.htm
ms.date: 12/05/2018
ms.keywords: PropSheet_PageToIndex, PropSheet_PageToIndex macro [Windows Controls], _win32_PropSheet_PageToIndex, _win32_PropSheet_PageToIndex_cpp, controls.PropSheet_PageToIndex, controls._win32_PropSheet_PageToIndex, prsht/PropSheet_PageToIndex
f1_keywords:
- prsht/PropSheet_PageToIndex
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
- PropSheet_PageToIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_PageToIndex macro


## -description


Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/psm-pagetoindex">PSM_PAGETOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

HPROPSHEETPAGE handle to the property sheet page.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propsheet_indextopage">PropSheet_IndexToPage</a>



<b>Reference</b>
 

 

