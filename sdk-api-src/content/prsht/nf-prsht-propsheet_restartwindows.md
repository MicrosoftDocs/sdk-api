---
UID: NF:prsht.PropSheet_RestartWindows
title: PropSheet_RestartWindows macro
author: windows-driver-content
description: Sends a PSM_RESTARTWINDOWS message indicating that Windows needs to be restarted for changes to take effect. You can use this macro or send the PSM_RESTARTWINDOWS message explicitly.
old-location: controls\PropSheet_RestartWindows.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_restartwindows.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PropSheet_RestartWindows, PropSheet_RestartWindows macro [Windows Controls], _win32_PropSheet_RestartWindows, _win32_PropSheet_RestartWindows_cpp, controls.PropSheet_RestartWindows, controls._win32_PropSheet_RestartWindows, prsht/PropSheet_RestartWindows
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Prsht.h
api_name:
-	PropSheet_RestartWindows
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PropSheet_RestartWindows macro


## -description


Sends a <a href="https://msdn.microsoft.com/5bf634ee-7408-45df-adb6-c5b947f6c47b">PSM_RESTARTWINDOWS</a> message indicating that Windows needs to be restarted for changes to take effect. You can use this macro or send the <b>PSM_RESTARTWINDOWS</b> message explicitly.


## -parameters




### -param hDlg

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



An application should send the <a href="https://msdn.microsoft.com/5bf634ee-7408-45df-adb6-c5b947f6c47b">PSM_RESTARTWINDOWS</a> message only in response to the <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> or <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> notification code.

The <a href="https://msdn.microsoft.com/5bf634ee-7408-45df-adb6-c5b947f6c47b">PSM_RESTARTWINDOWS</a> message causes the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function to return the ID_PSRESTARTWINDOWS value, but only if the user clicks the <b>OK</b> button to close the property sheet. It is the application's responsibility to restart Windows, which can be done by using the <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> function.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>


