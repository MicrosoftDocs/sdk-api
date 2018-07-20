---
UID: NF:prsht.PropSheet_GetResult
title: PropSheet_GetResult macro
author: windows-sdk-content
description: Used by modeless property sheets to retrieve the information returned to modal property sheets by PropertySheet. You can use this macro or sent the PSM_GETRESULT message explicitly.
old-location: controls\PropSheet_GetResult.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_getresult.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PropSheet_GetResult, PropSheet_GetResult macro [Windows Controls], _win32_PropSheet_GetResult, _win32_PropSheet_GetResult_cpp, controls.PropSheet_GetResult, controls._win32_PropSheet_GetResult, prsht/PropSheet_GetResult
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
 - PropSheet_GetResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_GetResult macro


## -description


Used by modeless property sheets to retrieve the information returned to modal property sheets by <a href="https://msdn.microsoft.com/library/Bb760811(v=VS.85).aspx">PropertySheet</a>. You can use this macro or sent the <a href="https://msdn.microsoft.com/library/Bb774579(v=VS.85).aspx">PSM_GETRESULT</a> message explicitly.


## -parameters




### -param hDlg

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet's dialog box.


## -remarks



To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The return value is identical to what <a href="https://msdn.microsoft.com/library/Bb760811(v=VS.85).aspx">PropertySheet</a> would have returned had this been a modal property sheet.


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80.</a> The <a href="https://msdn.microsoft.com/library/Bb760811(v=VS.85).aspx">PropertySheet</a> return value carries different information for modal and modeless property sheets. In some cases, modeless property sheets may need the information they would have received from <b>PropertySheet</b> if they had been modal. In particular, they may need to know whether ID_PSREBOOTSYSTEM or ID_PSRESTARTWINDOWS would have been returned.

For a modeless property sheet, your message loop should use <a href="https://msdn.microsoft.com/library/Bb774593(v=VS.85).aspx">PSM_ISDIALOGMESSAGE</a> to pass messages to the property sheet dialog box, and <a href="https://msdn.microsoft.com/library/Bb774578(v=VS.85).aspx">PSM_GETCURRENTPAGEHWND</a> to determine when to destroy the dialog box. When the user clicks the <b>OK</b> or <b>Cancel</b> button, <b>PSM_GETCURRENTPAGEHWND</b> returns <b>NULL</b>. You can then retrieve the value that a modal property sheet would have received from <a href="https://msdn.microsoft.com/library/Bb760811(v=VS.85).aspx">PropertySheet</a> by sending a <a href="https://msdn.microsoft.com/library/Bb774579(v=VS.85).aspx">PSM_GETRESULT</a> message.

<div class="alert"><b>Note</b>  This macro is not supported when using the Aero wizard style (<a href="https://msdn.microsoft.com/library/Bb774546(v=VS.85).aspx">PSH_AEROWIZARD</a>).</div>
<div> </div>


