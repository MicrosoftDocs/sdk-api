---
UID: NF:windowsx.Edit_LineFromChar
title: Edit_LineFromChar macro (windowsx.h)
author: windows-sdk-content
description: Gets the index of the line that contains the specified character index in a multiline edit or rich edit control. You can use this macro or send the EM_LINEFROMCHAR message explicitly.
old-location: controls\Edit_LineFromChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_linefromchar.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Edit_LineFromChar, Edit_LineFromChar macro [Windows Controls], _win32_Edit_LineFromChar, _win32_Edit_LineFromChar_cpp, controls.Edit_LineFromChar, controls._win32_Edit_LineFromChar, windowsx/Edit_LineFromChar
ms.topic: macro
f1_keywords: 
 - "windowsx/Edit_LineFromChar"
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
 - Edit_LineFromChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Edit_LineFromChar macro


## -description


Gets the index of the line that contains the specified character index in a multiline edit or rich edit control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param ich

Type: <b>int</b>

The zero-based index of the character from the beginning of the text in the control.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>.



