---
UID: NF:prsht.PropSheet_HwndToIndex
title: PropSheet_HwndToIndex macro
author: windows-sdk-content
description: Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the PSM_HWNDTOINDEX message explicitly.
old-location: controls\PropSheet_HwndToIndex.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_hwndtoindex.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PropSheet_HwndToIndex, PropSheet_HwndToIndex macro [Windows Controls], _win32_PropSheet_HwndToIndex, _win32_PropSheet_HwndToIndex_cpp, controls.PropSheet_HwndToIndex, controls._win32_PropSheet_HwndToIndex, prsht/PropSheet_HwndToIndex
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
 - PropSheet_HwndToIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_HwndToIndex macro


## -description


Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/2eda4c95-95ed-4ebf-8245-c5b96aeb9075">PSM_HWNDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hwnd

TBD






#### - hPageDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the page's window.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet's window.


## -see-also




<a href="https://msdn.microsoft.com/9e1991dd-e451-4f2a-ac9f-069acb8e89c2">GetParent</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b201025b-c468-4bfb-825b-63d59d1a62c8">PropSheet_GetCurrentPageHwnd</a>



<b>Reference</b>
 

 

