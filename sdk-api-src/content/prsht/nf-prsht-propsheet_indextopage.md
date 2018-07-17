---
UID: NF:prsht.PropSheet_IndexToPage
title: PropSheet_IndexToPage macro
author: windows-sdk-content
description: Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle. You can use this macro or send the PSM_INDEXTOPAGE message explicitly.
old-location: controls\PropSheet_IndexToPage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_indextopage.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PropSheet_IndexToPage, PropSheet_IndexToPage macro [Windows Controls], _win32_PropSheet_IndexToPage, _win32_PropSheet_IndexToPage_cpp, controls.PropSheet_IndexToPage, controls._win32_PropSheet_IndexToPage, prsht/PropSheet_IndexToPage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Prsht.h
api_name:
 - PropSheet_IndexToPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_IndexToPage macro


## -description


Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle. You can use this macro or send the <a href="https://msdn.microsoft.com/b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2">PSM_INDEXTOPAGE</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param i

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet window.


#### - iPageIndex

Type: <b>int</b>

Zero-based index of the page.


## -see-also




<a href="https://msdn.microsoft.com/e93d4d3f-a046-4f2b-8eab-91bf33c7cd1d">PropSheet_PageToIndex</a>
 

 

