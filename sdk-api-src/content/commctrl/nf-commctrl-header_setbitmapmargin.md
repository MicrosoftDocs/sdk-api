---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

