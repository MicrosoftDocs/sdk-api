---
UID: NF:windowsx.ScrollBar_GetPos
title: ScrollBar_GetPos macro (windowsx.h)
author: windows-sdk-content
description: Retrieves the position of the scroll box (thumb) in the specified scroll bar.
old-location: controls\ScrollBar_GetPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_getpos.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ScrollBar_GetPos, ScrollBar_GetPos macro [Windows Controls], _win32_ScrollBar_GetPos, _win32_ScrollBar_GetPos_cpp, controls.ScrollBar_GetPos, controls._win32_ScrollBar_GetPos, windowsx/ScrollBar_GetPos
ms.topic: macro
f1_keywords: 
 - "windowsx/ScrollBar_GetPos"
dev_langs:
 - c++
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
 - ScrollBar_GetPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ScrollBar_GetPos macro


## -description


Retrieves the position of the scroll box (thumb) in the specified scroll bar. 
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getscrollpos">GetScrollPos</a> function, which is deprecated. New applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getscrollinfo">GetScrollInfo</a>.



