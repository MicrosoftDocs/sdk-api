---
UID: NF:windowsx.Edit_ReplaceSel
title: Edit_ReplaceSel macro
author: windows-sdk-content
description: Replaces the selected text in an edit control or a rich edit control with the specified text. You can use this macro or send the EM_REPLACESEL message explicitly.
old-location: controls\Edit_ReplaceSel.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_replacesel.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Edit_ReplaceSel, Edit_ReplaceSel macro [Windows Controls], _win32_Edit_ReplaceSel, _win32_Edit_ReplaceSel_cpp, controls.Edit_ReplaceSel, controls._win32_Edit_ReplaceSel, windowsx/Edit_ReplaceSel
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
 - Edit_ReplaceSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_ReplaceSel macro


## -description


Replaces the selected text in an edit control or a rich edit control with the specified text. You can use this macro or send the <a href="https://msdn.microsoft.com/525e6f5a-f52f-4bab-bc76-caa484729897">EM_REPLACESEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpszReplace

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

A pointer to a null-terminated string containing the replacement text.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/525e6f5a-f52f-4bab-bc76-caa484729897">EM_REPLACESEL</a>.



