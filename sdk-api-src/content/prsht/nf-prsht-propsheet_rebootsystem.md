---
UID: NF:prsht.PropSheet_RebootSystem
title: PropSheet_RebootSystem macro
author: windows-sdk-content
description: Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the PSM_REBOOTSYSTEM message explicitly.
old-location: controls\PropSheet_RebootSystem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_rebootsystem.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PropSheet_RebootSystem, PropSheet_RebootSystem macro [Windows Controls], _win32_PropSheet_RebootSystem, _win32_PropSheet_RebootSystem_cpp, controls.PropSheet_RebootSystem, controls._win32_PropSheet_RebootSystem, prsht/PropSheet_RebootSystem
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
 - PropSheet_RebootSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_RebootSystem macro


## -description


Indicates the system needs to be restarted for the changes to take effect. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774601(v=VS.85).aspx">PSM_REBOOTSYSTEM</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



An application should send the PSM_REBOOTSYSTEM message only in response to the <a href="https://msdn.microsoft.com/en-us/library/Bb774552(v=VS.85).aspx">PSN_APPLY</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb774559(v=VS.85).aspx">PSN_KILLACTIVE</a> notification code.

This macro causes the <a href="https://msdn.microsoft.com/en-us/library/Bb760811(v=VS.85).aspx">PropertySheet</a> function to return the ID_PSREBOOTSYSTEM value, but only if the user clicks the <b>OK</b> button to close the property sheet. It is the application's responsibility to reboot the system, which can be done by using the <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> function.

This macro supersedes all <b>PropSheet_RebootSystem</b> macros that precede or follow it.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/en-us/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774607(v=VS.85).aspx">PSM_RESTARTWINDOWS</a>
 

 

