---
UID: NF:windowsx.Edit_SetWordBreakProc
title: Edit_SetWordBreakProc macro
author: windows-sdk-content
description: Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the EM_SETWORDBREAKPROC message explicitly.
old-location: controls\Edit_SetWordBreakProc.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setwordbreakproc.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Edit_SetWordBreakProc, Edit_SetWordBreakProc macro [Windows Controls], _win32_Edit_SetWordBreakProc, _win32_Edit_SetWordBreakProc_cpp, controls.Edit_SetWordBreakProc, controls._win32_Edit_SetWordBreakProc, windowsx/Edit_SetWordBreakProc
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
 - Edit_SetWordBreakProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetWordBreakProc macro


## -description


Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761665(v=VS.85).aspx">EM_SETWORDBREAKPROC</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpfnWordBreak

Type: <b>EDITWORDBREAKPROC</b>

The address of the application-defined Wordwrap function. For more information about breaking lines, see the description of the <a href="https://msdn.microsoft.com/en-us/library/Bb761709(v=VS.85).aspx">EditWordBreakProc</a> callback function. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761665(v=VS.85).aspx">EM_SETWORDBREAKPROC</a>.



