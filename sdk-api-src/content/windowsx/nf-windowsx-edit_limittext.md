---
UID: NF:windowsx.Edit_LimitText
title: Edit_LimitText macro
author: windows-sdk-content
description: Limits the length of text that can be entered into an edit control. You can use this macro or send the EM_LIMITTEXT message explicitly.
old-location: controls\Edit_LimitText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_limittext.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Edit_LimitText, Edit_LimitText macro [Windows Controls], _win32_Edit_LimitText, _win32_Edit_LimitText_cpp, controls.Edit_LimitText, controls._win32_Edit_LimitText, windowsx/Edit_LimitText
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
 - Edit_LimitText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_LimitText macro


## -description


Limits the length of text that can be entered into an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761607(v=VS.85).aspx">EM_LIMITTEXT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cchMax

Type: <b>int</b>

The maximum number of characters.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/Bb761607(v=VS.85).aspx">EM_LIMITTEXT</a>.



