---
UID: NF:prsht.PropSheet_GetCurrentPageHwnd
title: PropSheet_GetCurrentPageHwnd macro
author: windows-sdk-content
description: Retrieves a handle to the window of the current page of a property sheet. You can use this macro or send the PSM_GETCURRENTPAGEHWND message explicitly.
old-location: controls\PropSheet_GetCurrentPageHwnd.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_getcurrentpagehwnd.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PropSheet_GetCurrentPageHwnd, PropSheet_GetCurrentPageHwnd macro [Windows Controls], _win32_PropSheet_GetCurrentPageHwnd, _win32_PropSheet_GetCurrentPageHwnd_cpp, controls.PropSheet_GetCurrentPageHwnd, controls._win32_PropSheet_GetCurrentPageHwnd, prsht/PropSheet_GetCurrentPageHwnd
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PropSheet_GetCurrentPageHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_GetCurrentPageHwnd macro


## -description


Retrieves a handle to the window of the current page of a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/1f2d0af9-5853-48e7-b827-483be032b6ca">PSM_GETCURRENTPAGEHWND</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



Use the <b>PropSheet_GetCurrentPageHwnd</b> macro with modeless property sheets to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PropSheet_GetCurrentPageHwnd</b> returns <b>NULL</b>, and you can then use the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function to destroy the dialog box.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a>
 

 

