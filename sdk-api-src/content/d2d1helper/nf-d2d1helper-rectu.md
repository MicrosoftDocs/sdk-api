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

# RectU function


## -description


Creates a <a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a> structure that contains the specified dimensions.


## -parameters




### -param left

Type: <b>UINT32</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.


### -param top

Type: <b>UINT32</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.


### -param right

Type: <b>UINT32</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.


### -param bottom

Type: <b>UINT32</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.


## -returns



Type: <b><a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a></b>

A rectangle structure that contains the specified dimensions.



