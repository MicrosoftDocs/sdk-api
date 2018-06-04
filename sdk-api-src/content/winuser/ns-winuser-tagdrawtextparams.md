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

# tagDRAWTEXTPARAMS structure


## -description



The <b>DRAWTEXTPARAMS</b> structure contains extended formatting options for the <a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a> function.




## -struct-fields




### -field cbSize

The structure size, in bytes.


### -field iTabLength

The size of each tab stop, in units equal to the average character width.


### -field iLeftMargin

The left margin, in units equal to the average character width.


### -field iRightMargin

The right margin, in units equal to the average character width.


### -field uiLengthDrawn

Receives the number of characters processed by <a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a>, including white-space characters. The number can be the <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> or the index of the first line that falls below the drawing area. Note that <b>DrawTextEx</b> always processes the entire string if the DT_NOCLIP formatting flag is specified.


## -see-also




<a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

