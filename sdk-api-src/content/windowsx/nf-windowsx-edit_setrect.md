---
UID: NF:windowsx.Edit_SetRect
title: Edit_SetRect macro
author: windows-sdk-content
description: Sets the formatting rectangle of an edit control. You can use this macro or send the EM_SETRECT message explicitly.
old-location: controls\Edit_SetRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setrect.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Edit_SetRect, Edit_SetRect macro [Windows Controls], _win32_Edit_SetRect, _win32_Edit_SetRect_cpp, controls.Edit_SetRect, controls._win32_Edit_SetRect, windowsx/Edit_SetRect
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
-	Edit_SetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_SetRect macro


## -description


Sets the formatting rectangle of an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/4f576e94-3bd3-4416-a960-b7f22da963ea">EM_SETRECT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the new dimensions of the rectangle. If this parameter is <b>NULL</b>, the formatting rectangle is set to its default values. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/4f576e94-3bd3-4416-a960-b7f22da963ea">EM_SETRECT</a>.



