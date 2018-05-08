---
UID: NF:windowsx.Edit_LineIndex
title: Edit_LineIndex macro
author: windows-driver-content
description: Gets the character index of the first character of a specified line in a multiline edit or rich edit control. You can use this macro or send the EM_LINEINDEX message explicitly.
old-location: controls\Edit_LineIndex.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_lineindex.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: Edit_LineIndex, Edit_LineIndex macro [Windows Controls], _win32_Edit_LineIndex, _win32_Edit_LineIndex_cpp, controls.Edit_LineIndex, controls._win32_Edit_LineIndex, windowsx/Edit_LineIndex
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
-	Edit_LineIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_LineIndex macro


## -description


Gets the character index of the first character of a specified line in a multiline edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/a4c65012-d47f-4d87-bc7f-2002d07f5eea">EM_LINEINDEX</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param line

Type: <b>int</b>

The zero-based line number. A value of –1 specifies the current line number (the line that contains the caret).

