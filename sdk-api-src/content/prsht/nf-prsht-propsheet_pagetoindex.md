---
UID: NF:prsht.PropSheet_PageToIndex
title: PropSheet_PageToIndex macro
author: windows-sdk-content
description: Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the PSM_PAGETOINDEX message explicitly.
old-location: controls\PropSheet_PageToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_pagetoindex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropSheet_PageToIndex, PropSheet_PageToIndex macro [Windows Controls], _win32_PropSheet_PageToIndex, _win32_PropSheet_PageToIndex_cpp, controls.PropSheet_PageToIndex, controls._win32_PropSheet_PageToIndex, prsht/PropSheet_PageToIndex
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_PageToIndex macro


## -description


Takes the HPROPSHEETPAGE handle of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774595(v=VS.85).aspx">PSM_PAGETOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

HPROPSHEETPAGE handle to the property sheet page.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774658(v=VS.85).aspx">PropSheet_IndexToPage</a>



<b>Reference</b>
 

 

