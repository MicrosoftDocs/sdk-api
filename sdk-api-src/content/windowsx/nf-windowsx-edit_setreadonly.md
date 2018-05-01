---
UID: NF:windowsx.Edit_SetReadOnly
title: Edit_SetReadOnly macro
author: windows-driver-content
description: Sets or removes the read-only style (ES_READONLY) of an edit or rich edit control. You can use this macro or send the EM_SETREADONLY message explicitly.
old-location: controls\Edit_SetReadOnly.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setreadonly.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: Edit_SetReadOnly, Edit_SetReadOnly macro [Windows Controls], _win32_Edit_SetReadOnly, _win32_Edit_SetReadOnly_cpp, controls.Edit_SetReadOnly, controls._win32_Edit_SetReadOnly, windowsx/Edit_SetReadOnly
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
-	Edit_SetReadOnly
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_SetReadOnly macro


## -description


Sets or removes the read-only style (ES_READONLY) of an edit or rich edit control.  You can use this macro or send the <a href="https://msdn.microsoft.com/a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8">EM_SETREADONLY</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fReadOnly

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to set the control to read-only; <b>FALSE</b> to remove the read-only style.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8">EM_SETREADONLY</a>.



