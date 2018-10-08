---
UID: NF:prsht.PropSheet_SetTitle
title: PropSheet_SetTitle macro
author: windows-sdk-content
description: Sets the title of a property sheet. You can use this macro or send the PSM_SETTITLE message explicitly.
old-location: controls\PropSheet_SetTitle.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_settitle.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PropSheet_SetTitle, PropSheet_SetTitle macro [Windows Controls], _win32_PropSheet_SetTitle, _win32_PropSheet_SetTitle_cpp, controls.PropSheet_SetTitle, controls._win32_PropSheet_SetTitle, prsht/PropSheet_SetTitle
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
 - PropSheet_SetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_SetTitle macro


## -description


Sets the title of a property sheet. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774627(v=VS.85).aspx">PSM_SETTITLE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param wStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flag that indicates whether to include the prefix "Properties for" with the specified title string. If <i>dwStyle</i> is the PSH_PROPTITLE value, the prefix is included. Otherwise, the prefix is not used.


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to a buffer that contains the title string. If the <a href="https://msdn.microsoft.com/en-us/library/ms632657(v=VS.85).aspx">HIWORD</a> of this parameter is <b>NULL</b>, the property sheet loads the string resource specified in the <a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a>.


## -remarks



In an Aero Wizard, this macro can be used to change the title of an interior page dynamically; for example, when handling the <a href="https://msdn.microsoft.com/en-us/library/Bb774568(v=VS.85).aspx">PSN_SETACTIVE</a> notification.



