---
UID: NF:prsht.PropSheet_AddPage
title: PropSheet_AddPage macro
author: windows-sdk-content
description: Adds a new page to the end of an existing property sheet. You can use this macro or send the PSM_ADDPAGE message explicitly.
old-location: controls\PropSheet_AddPage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_addpage.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: PropSheet_AddPage, PropSheet_AddPage macro [Windows Controls], _win32_PropSheet_AddPage, _win32_PropSheet_AddPage_cpp, controls.PropSheet_AddPage, controls._win32_PropSheet_AddPage, prsht/PropSheet_AddPage
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
 - PropSheet_AddPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_AddPage macro


## -description


Adds a new page to the end of an existing property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/41f9a09e-6de6-466b-bdfa-c8c4e8f193e4">PSM_ADDPAGE</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to add. The page must have been created by a previous call to the <a href="https://msdn.microsoft.com/fb7ca67a-7dff-4e1d-a303-5da87d8bbd2b">CreatePropertySheetPage</a> function.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.

A number of messages and one function call occur while the property sheet is manipulating the list of pages. While this action is taking place, attempting to modify the list of pages will have unpredictable results. Accordingly, you should not use the <b>PropSheet_AddPage</b> macro in your implementation of <a href="https://msdn.microsoft.com/a1f77ead-99c7-4874-8c32-289775c86458">PropSheetPageProc</a> or while handling the following notifications and Microsoft Windows messages:

<ul>
<li>
<a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/75448852-8a5e-41a7-92b6-00692e771a06">PSN_RESET</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463">PSN_SETACTIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/089c0645-199b-4a90-9cbc-740f0cf3267d">WM_DESTROY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bc4f4718-1dab-48db-ae3b-5a81a7be2644">WM_INITDIALOG</a>
</li>
</ul>
If you need to modify a property sheet page while you are handling one of these messages or while <a href="https://msdn.microsoft.com/a1f77ead-99c7-4874-8c32-289775c86458">PropSheetPageProc</a> is in operation, post yourself a private Windows message. Your application will not receive that message until after the property sheet manager has finished its tasks. Then you can modify the list of pages.



