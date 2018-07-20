---
UID: NF:prsht.PropSheet_SetCurSel
title: PropSheet_SetCurSel macro
author: windows-sdk-content
description: Activates the specified page in a property sheet. You can use this macro or send the PSM_SETCURSEL message explicitly.
old-location: controls\PropSheet_SetCurSel.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setcursel.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PropSheet_SetCurSel, PropSheet_SetCurSel macro [Windows Controls], _win32_PropSheet_SetCurSel, _win32_PropSheet_SetCurSel_cpp, controls.PropSheet_SetCurSel, controls._win32_PropSheet_SetCurSel, prsht/PropSheet_SetCurSel
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
 - PropSheet_SetCurSel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_SetCurSel macro


## -description


Activates the specified page in a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774611(v=VS.85).aspx">PSM_SETCURSEL</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to activate. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.


### -param index

Type: <b>UINT</b>

Zero-based index of the page. An application can specify the index or the handle, or both. If both are specified, <i>hpage</i> takes precedence.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



The window that is losing the activation receives the <a href="https://msdn.microsoft.com/library/Bb774559(v=VS.85).aspx">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="https://msdn.microsoft.com/library/Bb774568(v=VS.85).aspx">PSN_SETACTIVE</a> notification code.



