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

# tagICONMETRICSW structure


## -description


Contains the scalable metrics associated with icons. This structure is used with the  <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function when the <b>SPI_GETICONMETRICS</b>  or <b>SPI_SETICONMETRICS</b> action is specified.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the structure, in bytes. 


### -field iHorzSpacing

Type: <b>int</b>

The horizontal space, in pixels, for each arranged icon. 


### -field iVertSpacing

Type: <b>int</b>

The vertical space, in pixels, for each arranged icon. 


### -field iTitleWrap

Type: <b>int</b>

If this member is nonzero, icon titles wrap to a new line. If this member is zero, titles do not wrap. 


### -field lfFont

Type: <b><a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a></b>

The font to use for icon titles. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

