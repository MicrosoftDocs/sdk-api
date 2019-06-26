---
UID: NF:windowsx.Edit_Undo
title: Edit_Undo macro (windowsx.h)
author: windows-sdk-content
description: Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the EM_UNDO message explicitly.
old-location: controls\Edit_Undo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_undo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Edit_Undo, Edit_Undo macro [Windows Controls], _win32_Edit_Undo, _win32_Edit_Undo_cpp, controls.Edit_Undo, controls._win32_Edit_Undo, windowsx/Edit_Undo
ms.topic: macro
f1_keywords: 
 - "windowsx/Edit_Undo"
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
 - Edit_Undo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_Undo macro


## -description


Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-undo">EM_UNDO</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-undo">EM_UNDO</a>.



