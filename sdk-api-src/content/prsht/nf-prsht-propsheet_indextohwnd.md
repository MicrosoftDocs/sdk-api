---
UID: NF:prsht.PropSheet_IndexToHwnd
title: PropSheet_IndexToHwnd macro
author: windows-sdk-content
description: Takes the index of a property sheet page and returns its window handle. You can use this macro or send the PSM_INDEXTOHWND message explicitly.
old-location: controls\PropSheet_IndexToHwnd.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_indextohwnd.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PropSheet_IndexToHwnd, PropSheet_IndexToHwnd macro [Windows Controls], _win32_PropSheet_IndexToHwnd, _win32_PropSheet_IndexToHwnd_cpp, controls.PropSheet_IndexToHwnd, controls._win32_PropSheet_IndexToHwnd, prsht/PropSheet_IndexToHwnd
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
 - PropSheet_IndexToHwnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropSheet_IndexToHwnd macro


## -description


Takes the index of a property sheet page and returns its window handle. You can use this macro or send the <a href="https://msdn.microsoft.com/93b46b4c-47f9-4ce8-8797-f3d4bd5248e9">PSM_INDEXTOHWND</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param i

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet page's window.


#### - iPageIndex

Type: <b>int</b>

Zero-based index of the page.


## -see-also




<a href="https://msdn.microsoft.com/a90c1ccc-f25e-476a-bdc5-f4fb568a3cb5">PropSheet_HwndToIndex</a>
 

 

