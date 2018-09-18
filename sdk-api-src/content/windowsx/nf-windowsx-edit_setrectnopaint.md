---
UID: NF:windowsx.Edit_SetRectNoPaint
title: Edit_SetRectNoPaint macro
author: windows-sdk-content
description: Sets the formatting rectangle of a multiline edit control. This macro is equivalent to Edit_SetRect, except that it does not redraw the edit control window. You can use this macro or send the EM_SETRECTNP message explicitly.
old-location: controls\Edit_SetRectNoPaint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setrectnopaint.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Edit_SetRectNoPaint, Edit_SetRectNoPaint macro [Windows Controls], _win32_Edit_SetRectNoPaint, _win32_Edit_SetRectNoPaint_cpp, controls.Edit_SetRectNoPaint, controls._win32_Edit_SetRectNoPaint, windowsx/Edit_SetRectNoPaint
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
 - Edit_SetRectNoPaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetRectNoPaint macro


## -description


Sets the formatting rectangle of a multiline edit control. This macro is equivalent to <a href="https://msdn.microsoft.com/8778dcc9-51d0-4ab8-8fc1-2eebcdf12c35">Edit_SetRect</a>, except that it does not redraw the edit control window. You can use this macro or send the <a href="https://msdn.microsoft.com/1ab497ca-023f-4c26-b92d-b441a0d7b90c">EM_SETRECTNP</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lprc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the dimensions of the rectangle. If this parameter is <b>NULL</b>, the formatting rectangle is set to its default values. 


## -remarks



<b>Rich Edit 3.0 and later.</b> This macro does not have full functionality, because it does not set the WPARAM of the message.

For more information, see <a href="https://msdn.microsoft.com/1ab497ca-023f-4c26-b92d-b441a0d7b90c">EM_SETRECTNP</a>.



