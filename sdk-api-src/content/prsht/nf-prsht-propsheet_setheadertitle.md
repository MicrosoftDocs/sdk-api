---
UID: NF:prsht.PropSheet_SetHeaderTitle
title: PropSheet_SetHeaderTitle macro
author: windows-sdk-content
description: Sets the title text for the header of a wizard's interior page. You can use this macro or send the PSM_SETHEADERTITLE message explicitly.
old-location: controls\PropSheet_SetHeaderTitle.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_setheadertitle.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropSheet_SetHeaderTitle, PropSheet_SetHeaderTitle macro [Windows Controls], _win32_PropSheet_SetHeaderTitle, _win32_PropSheet_SetHeaderTitle_cpp, controls.PropSheet_SetHeaderTitle, controls._win32_PropSheet_SetHeaderTitle, prsht/PropSheet_SetHeaderTitle
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
 - PropSheet_SetHeaderTitle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PropSheet_SetHeaderTitle macro


## -description


Sets the title text for the header of a wizard's interior page. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774623(v=VS.85).aspx">PSM_SETHEADERTITLE</a> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the wizard's window.


### -param index

Type: <b>int</b>

Zero-based index of the page.


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

New header title.


## -remarks



If you specify the current page, it will immediately be repainted to display the new title.



