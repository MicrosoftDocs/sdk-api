---
UID: NF:windowsx.Static_GetTextLength
title: Static_GetTextLength macro (windowsx.h)
description: Gets the number of characters in the text of a static control.helpviewer_keywords: ["Static_GetTextLength","Static_GetTextLength macro [Windows Controls]","_win32_Static_GetTextLength","_win32_Static_GetTextLength_cpp","controls.Static_GetTextLength","controls._win32_Static_GetTextLength","windowsx/Static_GetTextLength"]
old-location: controls\Static_GetTextLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_gettextlength.htm
ms.date: 12/05/2018
ms.keywords: Static_GetTextLength, Static_GetTextLength macro [Windows Controls], _win32_Static_GetTextLength, _win32_Static_GetTextLength_cpp, controls.Static_GetTextLength, controls._win32_Static_GetTextLength, windowsx/Static_GetTextLength
f1_keywords:
- windowsx/Static_GetTextLength
dev_langs:
- c++
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
- Static_GetTextLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Static_GetTextLength macro


## -description


Gets the number of characters in the text of a static control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


## -remarks



The macro expands to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha">GetWindowTextLength</a>.
	



