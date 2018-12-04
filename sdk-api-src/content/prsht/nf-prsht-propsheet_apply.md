---
UID: NF:prsht.PropSheet_Apply
title: PropSheet_Apply macro
author: windows-sdk-content
description: Simulates the selection of the Apply button, indicating that one or more pages have changed and the changes need to be validated and recorded. You can use this macro or send the PSM_APPLY message explicitly.
old-location: controls\PropSheet_Apply.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_apply.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: PropSheet_Apply, PropSheet_Apply macro [Windows Controls], _win32_PropSheet_Apply, _win32_PropSheet_Apply_cpp, controls.PropSheet_Apply, controls._win32_PropSheet_Apply, prsht/PropSheet_Apply
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
 - PropSheet_Apply
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_Apply macro


## -description


Simulates the selection of the <b>Apply</b> button, indicating that one or more pages have changed and the changes need to be validated and recorded. You can use this macro or send the <a href="https://msdn.microsoft.com/2948fb66-ad77-4552-88b6-455418515e4c">PSM_APPLY</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



The property sheet sends the <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> notification code to the current page. If the current page returns <b>FALSE</b>, the property sheet sends the <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> notification code to all active pages.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>


