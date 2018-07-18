---
UID: NF:windowsx.Edit_LineLength
title: Edit_LineLength macro
author: windows-sdk-content
description: Retrieves the length, in characters, of a line in an edit or rich edit control. You can use this macro or send the EM_LINELENGTH message explicitly.
old-location: controls\Edit_LineLength.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_linelength.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Edit_LineLength, Edit_LineLength macro [Windows Controls], _win32_Edit_LineLength, _win32_Edit_LineLength_cpp, controls.Edit_LineLength, controls._win32_Edit_LineLength, windowsx/Edit_LineLength
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
 - Edit_LineLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_LineLength macro


## -description


Retrieves the length, in characters, of a line in an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761613(v=VS.85).aspx">EM_LINELENGTH</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param line

Type: <b>int</b>

The zero-based index of the line.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/Bb761613(v=VS.85).aspx">EM_LINELENGTH</a>.



