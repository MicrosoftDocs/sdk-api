---
UID: NF:windowsx.Button_GetCheck
title: Button_GetCheck macro (windowsx.h)
author: windows-sdk-content
description: Gets the check state of a radio button or check box. You can use this macro or send the BM_GETCHECK message explicitly.
old-location: controls\Button_GetCheck.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_getcheck.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Button_GetCheck, Button_GetCheck macro [Windows Controls], _win32_Button_GetCheck, _win32_Button_GetCheck_cpp, controls.Button_GetCheck, controls._win32_Button_GetCheck, windowsx/Button_GetCheck
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
 - Button_GetCheck
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Button_GetCheck macro


## -description


Gets the check state of a radio button or check box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775986(v=VS.85).aspx">BM_GETCHECK</a> message explicitly. 



## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


## -remarks



If the button has a style other than those listed, the return value is zero. 
		



