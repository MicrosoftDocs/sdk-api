---
UID: NF:windowsx.Static_GetText
title: Static_GetText macro
author: windows-sdk-content
description: Gets the text of a static control.
old-location: controls\Static_GetText.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_gettext.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Static_GetText, Static_GetText macro [Windows Controls], _win32_Static_GetText, _win32_Static_GetText_cpp, controls.Static_GetText, controls._win32_Static_GetText, windowsx/Static_GetText
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Static_GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Static_GetText macro


## -description


Gets the text of a static control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to the buffer that will receive the text.


### -param cchMax

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the NULL terminator.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/461d2200-2e3a-4361-bb2e-9a29ed9f333f">GetWindowText</a>.
	



