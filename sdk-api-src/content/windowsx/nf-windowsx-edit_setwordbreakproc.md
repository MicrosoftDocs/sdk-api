---
UID: NF:windowsx.Edit_SetWordBreakProc
title: Edit_SetWordBreakProc macro
author: windows-driver-content
description: Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the EM_SETWORDBREAKPROC message explicitly.
old-location: controls\Edit_SetWordBreakProc.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setwordbreakproc.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windowsx.h
api_name:
-	Edit_SetWordBreakProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# Edit_SetWordBreakProc macro


## -description


Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the <a href="https://msdn.microsoft.com/e5029b75-5f35-43a5-876d-24e81605bb49">EM_SETWORDBREAKPROC</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpfnWordBreak

Type: <b>EDITWORDBREAKPROC</b>

The address of the application-defined Wordwrap function. For more information about breaking lines, see the description of the <a href="https://msdn.microsoft.com/601afaee-f5cd-4b25-b9c7-5c6868b75b3f">EditWordBreakProc</a> callback function. 



## -remarks



For more information, see <a href="https://msdn.microsoft.com/e5029b75-5f35-43a5-876d-24e81605bb49">EM_SETWORDBREAKPROC</a>.



