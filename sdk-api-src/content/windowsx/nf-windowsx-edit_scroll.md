---
UID: NF:windowsx.Edit_Scroll
title: Edit_Scroll macro (windowsx.h)
author: windows-sdk-content
description: Scrolls the text vertically in a multiline edit or rich edit control. You can use this macro or send the EM_SCROLL message explicitly.
old-location: controls\Edit_Scroll.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_scroll.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Edit_Scroll, Edit_Scroll macro [Windows Controls], _win32_Edit_Scroll, _win32_Edit_Scroll_cpp, controls.Edit_Scroll, controls._win32_Edit_Scroll, windowsx/Edit_Scroll
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
 - Edit_Scroll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_Scroll macro


## -description


Scrolls the text vertically in a multiline edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761635(v=VS.85).aspx">EM_SCROLL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param dv

Type: <b>int</b>

The amount to scroll vertically.


### -param dh

Type: <b>int</b>

The amount to scroll horizontally.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761635(v=VS.85).aspx">EM_SCROLL</a>.



