---
UID: NF:prsht.PropSheet_RemovePage
title: PropSheet_RemovePage macro
author: windows-sdk-content
description: Removes a page from a property sheet. You can use this macro or send the PSM_REMOVEPAGE message explicitly.
old-location: controls\PropSheet_RemovePage.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_removepage.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropSheet_RemovePage, PropSheet_RemovePage macro [Windows Controls], _win32_PropSheet_RemovePage, _win32_PropSheet_RemovePage_cpp, controls.PropSheet_RemovePage, controls._win32_PropSheet_RemovePage, prsht/PropSheet_RemovePage
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Prsht.h
api_name:
-	PropSheet_RemovePage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropSheet_RemovePage macro


## -description


Removes a page from a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/2f387e97-4db4-4ad5-8600-7325da674e33">PSM_REMOVEPAGE</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param index

Type: <b>int</b>

Zero-based index of the page to be removed.


### -param hpage

Type: <b>HPROPSHEETPAGE</b>

Handle to the page to be removed.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



An application can specify the page to be removed by assigning a value to either <i>index</i> or <i>hpage</i>. If values are assigned to both <i>index</i> and <i>hpage</i>, <i>hpage</i> takes precedence.

A number of messages and one function call occur while the property sheet is manipulating the list of pages. While this action is taking place, attempting to modify the list of pages will have unpredictable results. Accordingly, you should not use the <b>PropSheet_RemovePage</b> macro in your implementation of <a href="https://msdn.microsoft.com/a1f77ead-99c7-4874-8c32-289775c86458">PropSheetPageProc</a> or while handling the following notifications and Windows messages.

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

The following notifications are also affected by property sheet modification.

<ul>
<li>
<a href="https://msdn.microsoft.com/784f92e7-6f10-40fc-b513-bea022f13ae1">PSN_WIZBACK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ff5be154-f2d1-403d-8f22-8f6cacfb66b1">PSN_WIZNEXT</a>
</li>
</ul>
You can add or remove pages in response to these notifications, provided that you return (via DWL_MSGRESULT) a nonzero value to specify the desired new page. Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> might be sent to the wrong page.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>


