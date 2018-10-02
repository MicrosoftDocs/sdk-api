---
UID: NF:windowsx.Edit_GetLine
title: Edit_GetLine macro
author: windows-sdk-content
description: Retrieves a line of text from an edit or rich edit control. You can use this macro or send the EM_GETLINE message explicitly.
old-location: controls\Edit_GetLine.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getline.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Edit_GetLine, Edit_GetLine macro [Windows Controls], _win32_Edit_GetLine, _win32_Edit_GetLine_cpp, controls.Edit_GetLine, controls._win32_Edit_GetLine, windowsx/Edit_GetLine
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
 - Edit_GetLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_GetLine macro


## -description


Retrieves a line of text from an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/ff56d2c6-5013-46c6-90d8-ee2bdc9074b1">EM_GETLINE</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param line

Type: <b>int</b>

The zero-based index of the line. This parameter is ignored by a single-line edit control. 



### -param lpch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that receives the string.


### -param cchMax

Type: <b>int</b>

The maximum number of characters to be copied to the buffer.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/ff56d2c6-5013-46c6-90d8-ee2bdc9074b1">EM_GETLINE</a>




