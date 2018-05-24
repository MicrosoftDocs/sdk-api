---
UID: NF:windowsx.Edit_SetHandle
title: Edit_SetHandle macro
author: windows-driver-content
description: Sets the handle of the memory that will be used by a multiline edit control. You can use this macro or send the EM_SETHANDLE message explicitly.
old-location: controls\Edit_SetHandle.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_sethandle.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Edit_SetHandle, Edit_SetHandle macro [Windows Controls], _win32_Edit_SetHandle, _win32_Edit_SetHandle_cpp, controls.Edit_SetHandle, controls._win32_Edit_SetHandle, windowsx/Edit_SetHandle
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
-	Edit_SetHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_SetHandle macro


## -description


Sets the handle of the memory that will be used by a multiline edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/0eae9365-62af-4040-8a51-273997a00b81">EM_SETHANDLE</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param h

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HLOCAL</a></b>

A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory. If necessary, the control reallocates this memory. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/0eae9365-62af-4040-8a51-273997a00b81">EM_SETHANDLE</a>.



