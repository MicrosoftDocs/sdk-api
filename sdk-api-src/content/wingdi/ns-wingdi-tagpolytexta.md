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

# tagPOLYTEXTA structure


## -description



The <b>POLYTEXT</b> structure describes how the <a href="https://msdn.microsoft.com/643b4f6a-843f-4795-adc8-a90223bdc246">PolyTextOut</a> function should draw a string of text.




## -struct-fields




### -field x

The horizontal reference point for the string. The string is aligned to this point using the current text-alignment mode.


### -field y

The vertical reference point for the string. The string is aligned to this point using the current text-alignment mode.


### -field n

The <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> pointed to by <b>lpstr</b>.


### -field lpstr

Pointer to a string of text to be drawn by the <a href="https://msdn.microsoft.com/643b4f6a-843f-4795-adc8-a90223bdc246">PolyTextOut</a> function. This string need not be null-terminated, since <b>n</b> specifies the length of the string.


### -field uiFlags

Specifies whether the string is to be opaque or clipped and whether the string is accompanied by an array of character-width values. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ETO_OPAQUE</td>
<td>The rectangle for each string is to be opaqued with the current background color.</td>
</tr>
<tr>
<td>ETO_CLIPPED</td>
<td>Each string is to be clipped to its specified rectangle.</td>
</tr>
</table>
 


### -field rcl

A rectangle structure that contains the dimensions of the opaquing or clipping rectangle. This member is ignored if neither of the ETO_OPAQUE nor the ETO_CLIPPED value is specified for the <b>uiFlags</b> member.


### -field pdx

Pointer to an array containing the width value for each character in the string.


## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/643b4f6a-843f-4795-adc8-a90223bdc246">PolyTextOut</a>
 

 

