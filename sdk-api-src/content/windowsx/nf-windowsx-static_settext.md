---
UID: NF:windowsx.Static_SetText
title: Static_SetText macro (windowsx.h)
author: windows-sdk-content
description: Sets the text of a static control.
old-location: controls\Static_SetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_settext.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Static_SetText, Static_SetText macro [Windows Controls], _win32_Static_SetText, _win32_Static_SetText_cpp, controls.Static_SetText, controls._win32_Static_SetText, windowsx/Static_SetText
ms.topic: macro
f1_keywords: ["windowsx/Static_SetText"]
req.header: windowsx.h
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
 - Windowsx.h
api_name:
 - Static_SetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Static_SetText macro


## -description


Sets the text of a static control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param lpsz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a null-terminated string to be used as the static control text.


## -remarks



The macro expands to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>.	



