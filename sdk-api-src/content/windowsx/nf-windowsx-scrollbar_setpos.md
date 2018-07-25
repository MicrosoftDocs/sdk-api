---
UID: NF:windowsx.ScrollBar_SetPos
title: ScrollBar_SetPos macro
author: windows-sdk-content
description: Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.
old-location: controls\ScrollBar_SetPos.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_setpos.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ScrollBar_SetPos, ScrollBar_SetPos macro [Windows Controls], _win32_ScrollBar_SetPos, _win32_ScrollBar_SetPos_cpp, controls.ScrollBar_SetPos, controls._win32_ScrollBar_SetPos, windowsx/ScrollBar_SetPos
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
 - ScrollBar_SetPos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ScrollBar_SetPos macro


## -description


Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box. 
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://msdn.microsoft.com/library/Bb787597(v=VS.85).aspx">SetScrollPos</a> function, which is deprecated. New applications should use the <a href="https://msdn.microsoft.com/library/Bb787595(v=VS.85).aspx">SetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param pos

Type: <b>int</b>

The new position of the scroll box.


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to redraw the control; otherwise <b>FALSE</b>.

