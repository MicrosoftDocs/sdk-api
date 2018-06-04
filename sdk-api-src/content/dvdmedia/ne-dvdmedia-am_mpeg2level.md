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

# AM_MPEG2Level enumeration


## -description



Indicates an MPEG-2 video level as specified in the MPEG-2 video standard (ISO13818-2).




## -enum-fields




### -field AM_MPEG2Level_Low


            Low level.
          


### -field AM_MPEG2Level_Main


            Main level.
          


### -field AM_MPEG2Level_High1440


            High 1440 level.
          


### -field AM_MPEG2Level_High


            High level.
          


## -remarks



DVD MPEG-2 video decoders should support AM_MPEG2Level_Low or AM_MPEG2Level_Main.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

