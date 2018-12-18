---
UID: NF:prsht.PropSheet_HwndToIndex
title: PropSheet_HwndToIndex macro
author: windows-sdk-content
description: Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the PSM_HWNDTOINDEX message explicitly.
old-location: controls\PropSheet_HwndToIndex.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_hwndtoindex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropSheet_HwndToIndex, PropSheet_HwndToIndex macro [Windows Controls], _win32_PropSheet_HwndToIndex, _win32_PropSheet_HwndToIndex_cpp, controls.PropSheet_HwndToIndex, controls._win32_PropSheet_HwndToIndex, prsht/PropSheet_HwndToIndex
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
 - PropSheet_HwndToIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_HwndToIndex macro


## -description


Takes a window handle of the property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774581(v=VS.85).aspx">PSM_HWNDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet's window.


### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the page's window.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms633510(v=VS.85).aspx">GetParent</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774645(v=VS.85).aspx">PropSheet_GetCurrentPageHwnd</a>



<b>Reference</b>
 

 

