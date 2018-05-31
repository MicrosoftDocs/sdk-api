---
UID: NF:windowsx.Edit_GetTextLength
title: Edit_GetTextLength macro
author: windows-sdk-content
description: Gets the number of characters in the text of an edit control.
old-location: controls\Edit_GetTextLength.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_gettextlength.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Edit_GetTextLength, Edit_GetTextLength macro [Windows Controls], _win32_Edit_GetTextLength, _win32_Edit_GetTextLength_cpp, controls.Edit_GetTextLength, controls._win32_Edit_GetTextLength, windowsx/Edit_GetTextLength
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
-	Edit_GetTextLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_GetTextLength macro


## -description


Gets the number of characters in the text of an edit control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



The macro expands to a call to <a href="https://msdn.microsoft.com/dfd05c5b-2e60-4f4f-aa6b-53f723a048be">GetWindowTextLength</a>.
	



