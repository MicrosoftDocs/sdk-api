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

# Color::MakeARGB


## -description


The <b>Color::MakeARGB</b> method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.


## -parameters




### -param a [in]

Type: <b>BYTE</b>

Byte that specifies the alpha component. 


### -param r [in]

Type: <b>BYTE</b>

Byte that specifies the red component. 


### -param g [in]

Type: <b>BYTE</b>

Byte that specifies the green component. 


### -param b [in]

Type: <b>BYTE</b>

Byte that specifies the blue component. 


## -returns



Type: <strong>Type: <b>static</b>
</strong>

This method returns an <b>ARGB</b> value that holds the specified alpha, red, green, and blue components.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/b333bf7d-b212-43fd-8f86-d7bf73b6a3f4">Color::GetValue</a>



<a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a>
 

 

