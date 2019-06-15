---
UID: NF:windowsx.Edit_SetReadOnly
title: Edit_SetReadOnly macro (windowsx.h)
author: windows-sdk-content
description: Sets or removes the read-only style (ES_READONLY) of an edit or rich edit control. You can use this macro or send the EM_SETREADONLY message explicitly.
old-location: controls\Edit_SetReadOnly.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setreadonly.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Edit_SetReadOnly, Edit_SetReadOnly macro [Windows Controls], _win32_Edit_SetReadOnly, _win32_Edit_SetReadOnly_cpp, controls.Edit_SetReadOnly, controls._win32_Edit_SetReadOnly, windowsx/Edit_SetReadOnly
ms.topic: macro
f1_keywords: ["windowsx/Edit_SetReadOnly"]
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
 - Edit_SetReadOnly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_SetReadOnly macro


## -description


Sets or removes the read-only style (ES_READONLY) of an edit or rich edit control.  You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setreadonly">EM_SETREADONLY</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param fReadOnly

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to set the control to read-only; <b>FALSE</b> to remove the read-only style.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-setreadonly">EM_SETREADONLY</a>.



