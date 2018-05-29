---
UID: NF:commctrl.Header_GetItemRect
title: Header_GetItemRect macro
author: windows-sdk-content
description: Gets the bounding rectangle for a given item in a header control. You can use this macro or send the HDM_GETITEMRECT message explicitly.
old-location: controls\Header_GetItemRect.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemrect.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Header_GetItemRect, Header_GetItemRect macro [Windows Controls], _win32_Header_GetItemRect, _win32_Header_GetItemRect_cpp, commctrl/Header_GetItemRect, controls.Header_GetItemRect, controls._win32_Header_GetItemRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Header_GetItemRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_GetItemRect macro


## -description


Gets the bounding rectangle for a given item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/b483ef97-3700-425b-8160-81c673850f68">HDM_GETITEMRECT</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iItem

TBD


### -param lprc

TBD






#### - hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


#### - iIndex

Type: <b>int</b>

The zero-based index of the header control item for which to retrieve the bounding rectangle. 


#### - lpItemRect

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the bounding rectangle information. 

