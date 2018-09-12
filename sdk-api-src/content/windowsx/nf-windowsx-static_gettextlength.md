---
UID: NF:windowsx.Static_GetTextLength
title: Static_GetTextLength macro
author: windows-sdk-content
description: Gets the number of characters in the text of a static control.
old-location: controls\Static_GetTextLength.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_gettextlength.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Static_GetTextLength, Static_GetTextLength macro [Windows Controls], _win32_Static_GetTextLength, _win32_Static_GetTextLength_cpp, controls.Static_GetTextLength, controls._win32_Static_GetTextLength, windowsx/Static_GetTextLength
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Static_GetTextLength macro


## -description


Gets the number of characters in the text of a static control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/dfd05c5b-2e60-4f4f-aa6b-53f723a048be">GetWindowTextLength</a>.
	



