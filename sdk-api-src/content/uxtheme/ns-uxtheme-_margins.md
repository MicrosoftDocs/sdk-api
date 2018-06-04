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

# _MARGINS structure


## -description


Returned by the <a href="https://msdn.microsoft.com/bf588987-019b-402b-989c-8e868a697257">GetThemeMargins</a> function to define the margins of windows that have visual styles applied.


## -struct-fields




### -field cxLeftWidth

Type: <b>int</b>

Width of the left border that retains its size.


### -field cxRightWidth

Type: <b>int</b>

Width of the right border that retains its size.


### -field cyTopHeight

Type: <b>int</b>

Height of the top border that retains its size.


### -field cyBottomHeight

Type: <b>int</b>

Height of the bottom border that retains its size.


## -see-also




<a href="https://msdn.microsoft.com/bf588987-019b-402b-989c-8e868a697257">GetThemeMargins</a>
 

 

