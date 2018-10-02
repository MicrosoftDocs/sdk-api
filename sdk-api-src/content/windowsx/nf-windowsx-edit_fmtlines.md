---
UID: NF:windowsx.Edit_FmtLines
title: Edit_FmtLines macro
author: windows-sdk-content
description: Sets a flag that determines whether text retrieved from a multiline edit control includes soft line-break characters.
old-location: controls\Edit_FormatLines.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_formatlines.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Edit_FmtLines, Edit_FmtLines macro [Windows Controls], _win32_Edit_FormatLines, _win32_Edit_FormatLines_cpp, controls.Edit_FormatLines, controls._win32_Edit_FormatLines, windowsx/Edit_FmtLines
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
 - Edit_FmtLines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_FmtLines macro


## -description


Sets a flag that determines whether text retrieved from a multiline edit control includes soft line-break characters. A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761570(v=VS.85).aspx">EM_FMTLINES</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fAddEOL

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to insert line breaks; otherwise <b>FALSE</b>. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761570(v=VS.85).aspx">EM_FMTLINES</a>.



