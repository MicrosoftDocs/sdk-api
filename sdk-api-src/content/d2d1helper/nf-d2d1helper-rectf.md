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

# RectF function


## -description


Creates a <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a> structure that contains the specified dimensions.


## -parameters




### -param left

Type: <b>FLOAT</b>

The x-coordinate of the upper-left corner of the rectangle. The default value is 0.f.


### -param top

Type: <b>FLOAT</b>

The y-coordinate of the upper-left corner of the rectangle. The default value is 0.f.


### -param right

Type: <b>FLOAT</b>

The x-coordinate of the lower-right corner of the rectangle. The default value is 0.f.


### -param bottom

Type: <b>FLOAT</b>

The y-coordinate of the lower-right corner of the rectangle. The default value is 0.f.


## -returns



Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a></b>

A rectangle structure that contains the specified dimensions.



