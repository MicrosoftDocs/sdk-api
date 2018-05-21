---
UID: NF:windowsx.ScrollBar_GetPos
title: ScrollBar_GetPos macro
author: windows-driver-content
description: Retrieves the position of the scroll box (thumb) in the specified scroll bar.
old-location: controls\ScrollBar_GetPos.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarmacros\scrollbar_getpos.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ScrollBar_GetPos, ScrollBar_GetPos macro [Windows Controls], _win32_ScrollBar_GetPos, _win32_ScrollBar_GetPos_cpp, controls.ScrollBar_GetPos, controls._win32_ScrollBar_GetPos, windowsx/ScrollBar_GetPos
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
-	ScrollBar_GetPos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ScrollBar_GetPos macro


## -description


Retrieves the position of the scroll box (thumb) in the specified scroll bar. 
        
<div class="alert"><b>Note</b>  This macro expands to a call to the <a href="https://msdn.microsoft.com/8d8c43df-c444-4c0a-82e5-bdc568161561">GetScrollPos</a> function, which is deprecated. New applications should use the <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>.



