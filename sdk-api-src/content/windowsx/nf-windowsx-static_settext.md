---
UID: NF:windowsx.Static_SetText
title: Static_SetText macro
author: windows-sdk-content
description: Sets the text of a static control.
old-location: controls\Static_SetText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_settext.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Static_SetText, Static_SetText macro [Windows Controls], _win32_Static_SetText, _win32_Static_SetText_cpp, controls.Static_SetText, controls._win32_Static_SetText, windowsx/Static_SetText
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	Static_SetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Static_SetText macro


## -description


Sets the text of a static control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a null-terminated string to be used as the static control text.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/6f3e3ef8-b342-43f0-9d8b-3a72c610a940">SetWindowText</a>.	



