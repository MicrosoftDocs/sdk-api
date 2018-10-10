---
UID: NF:windowsx.ScrollBar_GetRange
title: ScrollBar_GetRange macro
author: windows-sdk-content
description: Gets the range of a scroll bar.
old-location: controls\ScrollBar_GetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_getrange.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ScrollBar_GetRange, ScrollBar_GetRange macro [Windows Controls], _win32_ScrollBar_GetRange, _win32_ScrollBar_GetRange_cpp, controls.ScrollBar_GetRange, controls._win32_ScrollBar_GetRange, windowsx/ScrollBar_GetRange
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
 - ScrollBar_GetRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScrollBar_GetRange macro


## -description


Gets the range of a scroll bar.
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://msdn.microsoft.com/en-us/library/Bb787587(v=VS.85).aspx">GetScrollRange</a> function, which is deprecated. New applications should use the <a href="https://msdn.microsoft.com/en-us/library/Bb787583(v=VS.85).aspx">GetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param lpposMin

Type: <b>int*</b>

Address of a variable that receives the minimum value of the scroll bar.


### -param lpposMax

Type: <b>int*</b>

Address of a variable that receives the maximum value of the scroll bar.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787587(v=VS.85).aspx">GetScrollRange</a>.



