---
UID: NF:prsht.PropSheet_RecalcPageSizes
title: PropSheet_RecalcPageSizes macro
author: windows-sdk-content
description: Recalculates the page size of a standard or wizard property sheet after pages have been added or removed. You can use this macro or send the PSM_RECALCPAGESIZES message explicitly.
old-location: controls\PropSheet_RecalcPageSizes.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_recalcpagesizes.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropSheet_RecalcPageSizes, PropSheet_RecalcPageSizes macro [Windows Controls], _win32_PropSheet_RecalcPageSizes, _win32_PropSheet_RecalcPageSizes_cpp, controls.PropSheet_RecalcPageSizes, controls._win32_PropSheet_RecalcPageSizes, prsht/PropSheet_RecalcPageSizes
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
 - PropSheet_RecalcPageSizes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_RecalcPageSizes macro


## -description


Recalculates the page size of a standard or wizard property sheet after pages have been added or removed. You can use this macro or send the <a href="https://msdn.microsoft.com/42257ea3-0471-4c67-adcd-01cd2669a51e">PSM_RECALCPAGESIZES</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet's dialog box.


## -remarks



When a property sheet is created, it is sized to fit its initial collection of pages. To maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed. With common controls <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 5.80</a> and later, applications should use the <b>PropSheet_RecalcPageSizes</b> macro after adding or removing pages with <a href="https://msdn.microsoft.com/341505ff-88ce-4548-a894-e87b5b0235fb">PropSheet_AddPage</a>, <a href="https://msdn.microsoft.com/40679750-7e93-43fe-bed5-d55544663746">PropSheet_InsertPage</a>, <a href="https://msdn.microsoft.com/adbb1c88-3457-4dc4-8cc0-7f6f164d3f3a">PropSheet_RemovePage</a>, or their equivalent messages. It ensures that the property sheet is properly sized for its current collection of pages. If this macro or the equivalent message is not used, some property sheet pages may be truncated or too large.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>


