---
UID: NF:prsht.PropSheet_GetCurrentPageHwnd
title: PropSheet_GetCurrentPageHwnd macro (prsht.h)
author: windows-sdk-content
description: Retrieves a handle to the window of the current page of a property sheet. You can use this macro or send the PSM_GETCURRENTPAGEHWND message explicitly.
old-location: controls\PropSheet_GetCurrentPageHwnd.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_getcurrentpagehwnd.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropSheet_GetCurrentPageHwnd, PropSheet_GetCurrentPageHwnd macro [Windows Controls], _win32_PropSheet_GetCurrentPageHwnd, _win32_PropSheet_GetCurrentPageHwnd_cpp, controls.PropSheet_GetCurrentPageHwnd, controls._win32_PropSheet_GetCurrentPageHwnd, prsht/PropSheet_GetCurrentPageHwnd
ms.topic: macro
f1_keywords: ["prsht/PropSheet_GetCurrentPageHwnd"]
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
 - PropSheet_GetCurrentPageHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_GetCurrentPageHwnd macro


## -description


Retrieves a handle to the window of the current page of a property sheet. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-getcurrentpagehwnd">PSM_GETCURRENTPAGEHWND</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


## -remarks



Use the <b>PropSheet_GetCurrentPageHwnd</b> macro with modeless property sheets to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PropSheet_GetCurrentPageHwnd</b> returns <b>NULL</b>, and you can then use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroywindow">DestroyWindow</a> function to destroy the dialog box.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-_propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a>
 

 

