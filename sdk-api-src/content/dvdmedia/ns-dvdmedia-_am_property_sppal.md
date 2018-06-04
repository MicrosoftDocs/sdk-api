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

# _AM_PROPERTY_SPPAL structure


## -description



Specifies the DVD subpicture palette.




## -struct-fields




### -field sppal

Array of 16 YUV elements that correspond to the 4-bit color numbers requested within the subpicture command stream. The YUV elements are of type <a href="https://msdn.microsoft.com/fb954bc2-4ef1-4a5f-b795-a3b2a8aae8d4">AM_DVD_YUV</a>.


## -remarks



The AM_PROPERTY_DVDSUBPIC_PALETTE property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/ddbfb65c-7630-4e9f-8013-c5d65c62c628">DVD Subpicture Property Set</a>
 

 

