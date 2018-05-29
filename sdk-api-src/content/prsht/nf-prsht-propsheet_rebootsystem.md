---
UID: NF:prsht.PropSheet_RebootSystem
title: PropSheet_RebootSystem macro
author: windows-sdk-content
description: Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the PSM_REBOOTSYSTEM message explicitly.
old-location: controls\PropSheet_RebootSystem.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_rebootsystem.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: PropSheet_RebootSystem, PropSheet_RebootSystem macro [Windows Controls], _win32_PropSheet_RebootSystem, _win32_PropSheet_RebootSystem_cpp, controls.PropSheet_RebootSystem, controls._win32_PropSheet_RebootSystem, prsht/PropSheet_RebootSystem
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
-	PropSheet_RebootSystem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropSheet_RebootSystem macro


## -description


Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the <a href="https://msdn.microsoft.com/461fce3c-183a-4b9b-8eab-ed2838d9f866">PSM_REBOOTSYSTEM</a> message explicitly.


## -parameters




### -param hDlg

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



An application should send the PSM_REBOOTSYSTEM message only in response to the <a href="https://msdn.microsoft.com/18da6bdb-9409-49b6-8116-580fedd99a02">PSN_APPLY</a> or <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> notification code.

This macro causes the <a href="https://msdn.microsoft.com/1cef9b14-498e-4dcb-94a5-5faa17e0774e">PropertySheet</a> function to return the ID_PSREBOOTSYSTEM value, but only if the user clicks the <b>OK</b> button to close the property sheet. It is the application's responsibility to reboot the system, which can be done by using the <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> function.

This macro supersedes all <b>PropSheet_RebootSystem</b> macros that precede or follow it.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/ed4eb370-593f-4893-9de4-1ea9a725b131">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5bf634ee-7408-45df-adb6-c5b947f6c47b">PSM_RESTARTWINDOWS</a>
 

 

