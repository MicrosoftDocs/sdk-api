---
UID: NF:prsht.PropSheet_SetTitle
title: PropSheet_SetTitle macro (prsht.h)
author: windows-sdk-content
description: Sets the title of a property sheet. You can use this macro or send the PSM_SETTITLE message explicitly.
old-location: controls\PropSheet_SetTitle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_settitle.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropSheet_SetTitle, PropSheet_SetTitle macro [Windows Controls], _win32_PropSheet_SetTitle, _win32_PropSheet_SetTitle_cpp, controls.PropSheet_SetTitle, controls._win32_PropSheet_SetTitle, prsht/PropSheet_SetTitle
ms.topic: macro
f1_keywords: 
 - "prsht/PropSheet_SetTitle"
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
 - PropSheet_SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_SetTitle macro


## -description


Sets the title of a property sheet. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-settitle">PSM_SETTITLE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


### -param wStyle

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flag that indicates whether to include the prefix "Properties for" with the specified title string. If <i>dwStyle</i> is the PSH_PROPTITLE value, the prefix is included. Otherwise, the prefix is not used.


### -param lpszText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a buffer that contains the title string. If the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> of this parameter is <b>NULL</b>, the property sheet loads the string resource specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a>.


## -remarks



In an Aero Wizard, this macro can be used to change the title of an interior page dynamically; for example, when handling the <a href="https://docs.microsoft.com/windows/desktop/Controls/psn-setactive">PSN_SETACTIVE</a> notification.



