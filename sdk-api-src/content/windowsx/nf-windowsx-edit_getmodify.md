---
UID: NF:windowsx.Edit_GetModify
title: Edit_GetModify macro
author: windows-sdk-content
description: Gets the state of an edit or rich edit control's modification flag. The flag indicates whether the contents of the control have been modified. You can use this macro or send the EM_GETMODIFY message explicitly.
old-location: controls\Edit_GetModify.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getmodify.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Edit_GetModify, Edit_GetModify macro [Windows Controls], _win32_Edit_GetModify, _win32_Edit_GetModify_cpp, controls.Edit_GetModify, controls._win32_Edit_GetModify, windowsx/Edit_GetModify
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
-	Edit_GetModify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_GetModify macro


## -description


Gets the state of an edit or rich edit control's modification flag. The flag indicates whether the contents of the control have been modified. You can use this macro or send the <a href="https://msdn.microsoft.com/4229e2f2-3493-4721-8b52-8933c9dc0a77">EM_GETMODIFY</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/4229e2f2-3493-4721-8b52-8933c9dc0a77">EM_GETMODIFY</a>.



