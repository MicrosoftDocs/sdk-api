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

# _AM_PROPERTY_SPHLI structure


## -description



Describes the currently selected button from the DVD highlight information.




## -struct-fields




### -field HLISS

Highlight status of current selection.


### -field Reserved

Reserved for internal use. Do not use or set.


### -field StartPTM

Start presentation time divided by 90,000.


### -field EndPTM

End presentation time divided by 90,000.


### -field StartX

Start x-coordinate pixel of the current highlight button.


### -field StartY

Start y-coordinate pixel of the current highlight button.


### -field StopX

Ending x-coordinate pixel of the current highlight button.


### -field StopY

Ending y-coordinate pixel of the current highlight button.


### -field ColCon

Color contrast description of type <a href="https://msdn.microsoft.com/9358d860-6187-48d9-81b6-d5d65d73786d">AM_COLCON</a>.


## -remarks



The <b>AM_PROPERTY_DVDSUBPIC_HLI</b> property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/ddbfb65c-7630-4e9f-8013-c5d65c62c628">DVD Subpicture Property Set</a>
 

 

