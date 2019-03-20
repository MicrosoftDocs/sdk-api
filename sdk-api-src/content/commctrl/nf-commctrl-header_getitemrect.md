---
UID: NF:commctrl.Header_GetItemRect
title: Header_GetItemRect macro (commctrl.h)
author: windows-sdk-content
description: Gets the bounding rectangle for a given item in a header control. You can use this macro or send the HDM_GETITEMRECT message explicitly.
old-location: controls\Header_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_getitemrect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Header_GetItemRect, Header_GetItemRect macro [Windows Controls], _win32_Header_GetItemRect, _win32_Header_GetItemRect_cpp, commctrl/Header_GetItemRect, controls.Header_GetItemRect, controls._win32_Header_GetItemRect
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_GetItemRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_GetItemRect macro


## -description


Gets the bounding rectangle for a given item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775341(v=VS.85).aspx">HDM_GETITEMRECT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param iItem

Type: <b>int</b>

The zero-based index of the header control item for which to retrieve the bounding rectangle. 


### -param lprc

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the bounding rectangle information. 

