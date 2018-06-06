---
UID: NF:windowsx.Edit_Undo
title: Edit_Undo macro
author: windows-sdk-content
description: Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the EM_UNDO message explicitly.
old-location: controls\Edit_Undo.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_undo.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Edit_Undo, Edit_Undo macro [Windows Controls], _win32_Edit_Undo, _win32_Edit_Undo_cpp, controls.Edit_Undo, controls._win32_Edit_Undo, windowsx/Edit_Undo
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
 - Edit_Undo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_Undo macro


## -description


Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/c4bff128-0383-40c5-8f29-7738f7f26871">EM_UNDO</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/c4bff128-0383-40c5-8f29-7738f7f26871">EM_UNDO</a>.



