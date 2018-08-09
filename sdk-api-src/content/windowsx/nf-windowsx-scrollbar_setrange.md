---
UID: NF:windowsx.ScrollBar_SetRange
title: ScrollBar_SetRange macro
author: windows-sdk-content
description: Sets the range of a scroll bar.
old-location: controls\ScrollBar_SetRange.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_setrange.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ScrollBar_SetRange, ScrollBar_SetRange macro [Windows Controls], _win32_ScrollBar_SetRange, _win32_ScrollBar_SetRange_cpp, controls.ScrollBar_SetRange, controls._win32_ScrollBar_SetRange, windowsx/ScrollBar_SetRange
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
 - ScrollBar_SetRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ScrollBar_SetRange macro


## -description


Sets the range of a scroll bar.
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://msdn.microsoft.com/en-us/library/Bb787599(v=VS.85).aspx">SetScrollRange</a> function, which is deprecated. New applications should use the <a href="https://msdn.microsoft.com/en-us/library/Bb787595(v=VS.85).aspx">SetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param posMin

Type: <b>int</b>

The minimum value of the scroll bar.


### -param posMax

Type: <b>int</b>

The maximum value of the scroll bar.


### -param fRedraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to redraw the control; otherwise <b>FALSE</b>.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787599(v=VS.85).aspx">SetScrollRange</a>.



