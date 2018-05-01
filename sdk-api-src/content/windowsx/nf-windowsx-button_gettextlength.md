---
UID: NF:windowsx.Button_GetTextLength
title: Button_GetTextLength macro
author: windows-driver-content
description: Gets the number of characters in the text of a button.
old-location: controls\Button_GetTextLength.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_gettextlength.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: Button_GetTextLength, Button_GetTextLength macro [Windows Controls], _win32_Button_GetTextLength, _win32_Button_GetTextLength_cpp, controls.Button_GetTextLength, controls._win32_Button_GetTextLength, windowsx/Button_GetTextLength
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	Button_GetTextLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Button_GetTextLength macro


## -description


Gets the number of characters in the text of a button.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/dfd05c5b-2e60-4f4f-aa6b-53f723a048be">GetWindowTextLength</a>.
	



