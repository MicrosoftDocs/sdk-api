---
UID: NF:prsht.PropSheet_CancelToClose
title: PropSheet_CancelToClose macro
author: windows-sdk-content
description: Used when changes made since the most recent PSN_APPLY notification cannot be canceled. You can also send a PSM_CANCELTOCLOSE message explicitly.
old-location: controls\PropSheet_CancelToClose.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_canceltoclose.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropSheet_CancelToClose, PropSheet_CancelToClose macro [Windows Controls], _win32_PropSheet_CancelToClose, _win32_PropSheet_CancelToClose_cpp, controls.PropSheet_CancelToClose, controls._win32_PropSheet_CancelToClose, prsht/PropSheet_CancelToClose
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
-	PropSheet_CancelToClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropSheet_CancelToClose macro


## -description


Used when changes made since the most recent <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> notification cannot be canceled. You can also send a <a href="https://msdn.microsoft.com/0a4b6176-7ddb-469f-8ebf-a31e533a8690">PSM_CANCELTOCLOSE</a> message explicitly.


## -parameters




### -param hDlg

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks




<a href="https://msdn.microsoft.com/0a4b6176-7ddb-469f-8ebf-a31e533a8690">PSM_CANCELTOCLOSE</a> disables the <b>Cancel</b> button and changes the text of the <b>OK</b> button to "Close". You can use this macro or send the <b>PSM_CANCELTOCLOSE</b> message explicitly.

Most property sheets wait to perform irreversible changes until a <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> notification is received. However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN_APPLY/<a href="https://msdn.microsoft.com/75448852-8a5e-41a7-92b6-00692e771a06">PSN_RESET</a> sequence. One example is a property sheet that contains an <b>Edit</b> button that is used to display a subdialog box for editing a property. When the user clicks <b>OK</b> to submit the change, the property sheet page has several options:

<ul>
<li>It can record the changes but wait until it receives a <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> notification to apply them. This is the preferred approach.</li>
<li>It can apply the changes immediately after exiting the subdialog box, but remember the original settings. Those settings can be used to restore the original state if a <a href="https://msdn.microsoft.com/75448852-8a5e-41a7-92b6-00692e771a06">PSN_RESET</a> notification is received.</li>
<li>It can apply the changes immediately and not attempt to restore the original settings when it receives a <a href="https://msdn.microsoft.com/75448852-8a5e-41a7-92b6-00692e771a06">PSN_RESET</a> notification. This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</li>
</ul>
For the third option, applications should send a <a href="https://msdn.microsoft.com/0a4b6176-7ddb-469f-8ebf-a31e533a8690">PSM_CANCELTOCLOSE</a> message to the property sheet. It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the <b>Cancel</b> button.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>


