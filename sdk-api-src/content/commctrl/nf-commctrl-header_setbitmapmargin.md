---
UID: NF:commctrl.Header_SetBitmapMargin
title: Header_SetBitmapMargin macro
author: windows-sdk-content
description: Sets the width of the margin for a bitmap in an existing header control. You can use this macro or send the HDM_SETBITMAPMARGIN message explicitly.
old-location: controls\Header_SetBitmapMargin.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setbitmapmargin.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: Header_SetBitmapMargin, Header_SetBitmapMargin macro [Windows Controls], _win32_Header_SetBitmapMargin, _win32_Header_SetBitmapMargin_cpp, commctrl/Header_SetBitmapMargin, controls.Header_SetBitmapMargin, controls._win32_Header_SetBitmapMargin
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Header_SetBitmapMargin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_SetBitmapMargin macro


## -description


Sets the width of the margin for a bitmap in an existing header control. You can use this macro or send the <a href="https://msdn.microsoft.com/5ac04701-18c8-42d4-9850-fe6eb813672c">HDM_SETBITMAPMARGIN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param iWidth

Type: <b>int</b>

The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control. 


## -see-also




<a href="https://msdn.microsoft.com/3590cbdd-03fc-4654-8a8d-63d62d3f27a8">Header_GetBitmapMargin</a>
 

 

