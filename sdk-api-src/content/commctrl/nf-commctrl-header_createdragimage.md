---
UID: NF:commctrl.Header_CreateDragImage
title: Header_CreateDragImage macro (commctrl.h)
description: Creates a transparent version of an item image within an existing header control. You can use this macro or send the HDM_CREATEDRAGIMAGE message explicitly.
helpviewer_keywords: ["Header_CreateDragImage","Header_CreateDragImage macro [Windows Controls]","_win32_Header_CreateDragImage","_win32_Header_CreateDragImage_cpp","commctrl/Header_CreateDragImage","controls.Header_CreateDragImage","controls._win32_Header_CreateDragImage"]
old-location: controls\Header_CreateDragImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_createdragimage.htm
ms.date: 12/05/2018
ms.keywords: Header_CreateDragImage, Header_CreateDragImage macro [Windows Controls], _win32_Header_CreateDragImage, _win32_Header_CreateDragImage_cpp, commctrl/Header_CreateDragImage, controls.Header_CreateDragImage, controls._win32_Header_CreateDragImage
f1_keywords:
- commctrl/Header_CreateDragImage
dev_langs:
- c++
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
- Header_CreateDragImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Header_CreateDragImage macro


## -description


Creates a transparent version of an item image within an existing header control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-createdragimage">HDM_CREATEDRAGIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control. 


### -param i

Type: <b>int</b>

A zero-based index of the item within the header control. The image assigned to this item is used as the basis for the transparent image. 

