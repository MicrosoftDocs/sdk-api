---
UID: NF:prsht.PropSheet_SetCurSelByID
title: PropSheet_SetCurSelByID macro
author: windows-sdk-content
description: Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the PSM_SETCURSELID message explicitly.
old-location: controls\PropSheet_SetCurSelByID.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setcurselbyid.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PropSheet_SetCurSelByID, PropSheet_SetCurSelByID macro [Windows Controls], _win32_PropSheet_SetCurSelByID, _win32_PropSheet_SetCurSelByID_cpp, controls.PropSheet_SetCurSelByID, controls._win32_PropSheet_SetCurSelByID, prsht/PropSheet_SetCurSelByID
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
 - PropSheet_SetCurSelByID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_SetCurSelByID macro


## -description


Activates the specified page in a property sheet based on the resource identifier of the page. You can use this macro or send the <a href="https://msdn.microsoft.com/6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa">PSM_SETCURSELID</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param id

Type: <b>int</b>

Resource identifier of the page to activate.


## -remarks



The window that is losing the activation receives the <a href="https://msdn.microsoft.com/470cd6ff-73ad-451a-a861-4d3324a8a8db">PSN_KILLACTIVE</a> notification code, and the window that is gaining the activation receives the <a href="https://msdn.microsoft.com/0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463">PSN_SETACTIVE</a> notification code.



