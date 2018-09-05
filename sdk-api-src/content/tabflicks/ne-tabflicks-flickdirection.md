---
UID: NE:tabflicks.FLICKDIRECTION
title: FLICKDIRECTION
author: windows-sdk-content
description: Defines the directions in which a pen flick has occurred.
old-location: tablet\flickdirection.htm
old-project: tablet
ms.assetid: 49b282cb-45e6-4f80-9948-fd736c091e70
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 49b282cb-45e6-4f80-9948-fd736c091e70, FLICKDIRECTION, FLICKDIRECTION enumeration [Tablet PC], FLICKDIRECTION_DOWN, FLICKDIRECTION_DOWNLEFT, FLICKDIRECTION_DOWNRIGHT, FLICKDIRECTION_INVALID, FLICKDIRECTION_LEFT, FLICKDIRECTION_RIGHT, FLICKDIRECTION_UP, FLICKDIRECTION_UPLEFT, FLICKDIRECTION_UPRIGHT, tabflicks/FLICKDIRECTION, tabflicks/FLICKDIRECTION_DOWN, tabflicks/FLICKDIRECTION_DOWNLEFT, tabflicks/FLICKDIRECTION_DOWNRIGHT, tabflicks/FLICKDIRECTION_INVALID, tabflicks/FLICKDIRECTION_LEFT, tabflicks/FLICKDIRECTION_RIGHT, tabflicks/FLICKDIRECTION_UP, tabflicks/FLICKDIRECTION_UPLEFT, tabflicks/FLICKDIRECTION_UPRIGHT, tablet.flickdirection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tabflicks.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FLICKDIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tabflicks.h
api_name:
 - FLICKDIRECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# FLICKDIRECTION enumeration


## -description



Defines the directions in which a pen flick has occurred.




## -enum-fields




### -field FLICKDIRECTION_MIN


### -field FLICKDIRECTION_RIGHT

 A pen flick to the right.


### -field FLICKDIRECTION_UPRIGHT

 A pen flick to the upper right.


### -field FLICKDIRECTION_UP

 An upward pen flick.


### -field FLICKDIRECTION_UPLEFT

A pen flick to the upper left.


### -field FLICKDIRECTION_LEFT

A pen flick to the left.


### -field FLICKDIRECTION_DOWNLEFT

A pen flick to the lower left.


### -field FLICKDIRECTION_DOWN

A downward pen flick.


### -field FLICKDIRECTION_DOWNRIGHT

A pen flick to the down right.


### -field FLICKDIRECTION_INVALID

An invalid pen flick.


## -remarks



A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion. A flick is characterized by high speed and a high degree of straightness. A flick is identified by its direction. Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.




## -see-also




<a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">FLICK_DATA Structure</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">Flicks Gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">Responding to Pen Flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">WM_TABLET_FLICK Message</a>
 

 

