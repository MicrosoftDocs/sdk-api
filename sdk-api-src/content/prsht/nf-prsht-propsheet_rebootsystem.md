---
UID: NF:prsht.PropSheet_RebootSystem
title: PropSheet_RebootSystem macro (prsht.h)
author: windows-sdk-content
description: Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the PSM_REBOOTSYSTEM message explicitly.
old-location: controls\PropSheet_RebootSystem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_rebootsystem.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropSheet_RebootSystem, PropSheet_RebootSystem macro [Windows Controls], _win32_PropSheet_RebootSystem, _win32_PropSheet_RebootSystem_cpp, controls.PropSheet_RebootSystem, controls._win32_PropSheet_RebootSystem, prsht/PropSheet_RebootSystem
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
 - PropSheet_RebootSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropSheet_RebootSystem macro


## -description


Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/psm-rebootsystem">PSM_REBOOTSYSTEM</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the property sheet.


## -remarks



An application should send the PSM_REBOOTSYSTEM message only in response to the <a href="https://docs.microsoft.com/windows/desktop/Controls/psn-apply">PSN_APPLY</a> or <a href="https://docs.microsoft.com/windows/desktop/Controls/psn-killactive">PSN_KILLACTIVE</a> notification code.

This macro causes the <a href="https://docs.microsoft.com/windows/desktop/api/prsht/nf-prsht-propertysheeta">PropertySheet</a> function to return the ID_PSREBOOTSYSTEM value, but only if the user clicks the <b>OK</b> button to close the property sheet. It is the application's responsibility to reboot the system, which can be done by using the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function.

This macro supersedes all <b>PropSheet_RebootSystem</b> macros that precede or follow it.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://docs.microsoft.com/windows/desktop/api/prsht/ns-prsht-_propsheetheadera_v2">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/psm-restartwindows">PSM_RESTARTWINDOWS</a>
 

 

