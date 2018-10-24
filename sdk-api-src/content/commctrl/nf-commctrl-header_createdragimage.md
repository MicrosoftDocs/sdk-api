---
UID: NF:commctrl.Header_CreateDragImage
title: Header_CreateDragImage macro
author: windows-sdk-content
description: Creates a transparent version of an item image within an existing header control. You can use this macro or send the HDM_CREATEDRAGIMAGE message explicitly.
old-location: controls\Header_CreateDragImage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_createdragimage.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Header_CreateDragImage, Header_CreateDragImage macro [Windows Controls], _win32_Header_CreateDragImage, _win32_Header_CreateDragImage_cpp, commctrl/Header_CreateDragImage, controls.Header_CreateDragImage, controls._win32_Header_CreateDragImage
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Header_CreateDragImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_CreateDragImage macro


## -description


Creates a transparent version of an item image within an existing header control. You can use this macro or send the <a href="https://msdn.microsoft.com/1b9dc515-d327-4634-a424-cc15a32f0f7c">HDM_CREATEDRAGIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param i

Type: <b>int</b>

A zero-based index of the item within the header control. The image assigned to this item is used as the basis for the transparent image. 

