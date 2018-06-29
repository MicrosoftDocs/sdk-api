---
UID: NF:prsht.PropSheet_SetCurSelByID
title: PropSheet_SetCurSelByID macro
author: windows-sdk-content
description: Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the PSM_SETCURSELID message explicitly.
old-location: controls\PropSheet_SetCurSelByID.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setcurselbyid.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PropSheet_SetCurSelByID, PropSheet_SetCurSelByID macro [Windows Controls], _win32_PropSheet_SetCurSelByID, _win32_PropSheet_SetCurSelByID_cpp, controls.PropSheet_SetCurSelByID, controls._win32_PropSheet_SetCurSelByID, prsht/PropSheet_SetCurSelByID
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
 - PropSheet_SetCurSelByID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_SetCurSelByID macro


## -description


Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774613(v=VS.85).aspx">PSM_SETCURSELID</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param id

Type: <b>int</b>

Resource identifier of the page to activate.


#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


## -remarks



The window that is losing the activation receives the <a href="https://msdn.microsoft.com/library/Bb774559(v=VS.85).aspx">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="https://msdn.microsoft.com/library/Bb774568(v=VS.85).aspx">PSN_SETACTIVE</a> notification code.



