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

# ColorMatrixFlags enumeration


## -description


The <b>ColorMatrixFlags</b> enumeration specifies the types of images and colors that will be affected by the color and grayscale adjustment settings of an 
			<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object.


## -enum-fields




### -field ColorMatrixFlagsDefault

Specifies that all color values (including grays) are adjusted by the same color-adjustment matrix. 


### -field ColorMatrixFlagsSkipGrays

Specifies that colors are adjusted but gray shades are not adjusted. A gray shade is any color that has the same value for its red, green, and blue components. 


### -field ColorMatrixFlagsAltGray

Specifies that colors are adjusted by one matrix and gray shades are adjusted by another matrix. 


## -see-also




<a href="https://msdn.microsoft.com/4f98fe5b-a1fc-417c-ba08-ddcf0648de21">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/2043d592-e79a-45ce-8964-25ed245e4373">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/e0e00985-e422-4775-8ee2-a17d97214a25">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/6fe73738-41f6-4ff3-bcd5-a885040bf48b">ImageAttributes::SetColorMatrix</a>
 

 

