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

# Color::SetValue


## -description


The <b>Color::SetValue</b> method sets the color of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object.


## -parameters




### -param argb [in]

Type: <b>ARGB</b>

Thirty-two bit <b>ARGB</b> value that specifies the color. An <b>ARGB</b> value consolidates the alpha, red, green, and blue components of a color. <b>ARGB</b> is defined in Gdipluspixelformats.h. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/b333bf7d-b212-43fd-8f86-d7bf73b6a3f4">Color::GetValue</a>



<a href="https://msdn.microsoft.com/41befc00-c256-4f56-90c3-8fd5aa18bb49">Color::MakeARGB</a>
 

 

