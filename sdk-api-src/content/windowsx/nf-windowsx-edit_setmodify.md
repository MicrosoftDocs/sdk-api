---
UID: NF:windowsx.Edit_SetModify
title: Edit_SetModify macro
author: windows-sdk-content
description: Sets or clears the modification flag for an edit control. The modification flag indicates whether the text within the edit control has been modified. You can use this macro or send the EM_SETMODIFY message explicitly.
old-location: controls\Edit_SetModify.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setmodify.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Edit_SetModify, Edit_SetModify macro [Windows Controls], _win32_Edit_SetModify, _win32_Edit_SetModify_cpp, controls.Edit_SetModify, controls._win32_Edit_SetModify, windowsx/Edit_SetModify
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
 - Edit_SetModify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_SetModify macro


## -description


Sets or clears the modification flag for an edit control. The modification flag indicates whether the text within the edit control has been modified. You can use this macro or send the <a href="https://msdn.microsoft.com/9393f03e-0719-458b-8122-616df738c417">EM_SETMODIFY</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fModified

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the text has been modified; otherwise <b>FALSE</b>.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/9393f03e-0719-458b-8122-616df738c417">EM_SETMODIFY</a>.



