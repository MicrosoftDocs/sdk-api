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

# DWRITE_BREAK_CONDITION enumeration


## -description



	 Indicates the condition at the edges of inline object or text used to determine line-breaking behavior.


## -enum-fields




### -field DWRITE_BREAK_CONDITION_NEUTRAL


				
				Indicates whether a break is allowed by determining  the condition of the neighboring text span or inline object.


### -field DWRITE_BREAK_CONDITION_CAN_BREAK


     Indicates that a line break is allowed, unless overruled by the condition of the
     neighboring text span or inline object, either prohibited by a
     "may not break" condition or forced by a "must break" condition.				
				


### -field DWRITE_BREAK_CONDITION_MAY_NOT_BREAK


		     Indicates that there should be no line  break, unless overruled by a "must break" condition from
     the neighboring text span or inline object.		
				


### -field DWRITE_BREAK_CONDITION_MUST_BREAK


	     Indicates that the line break must happen, regardless of the condition of the adjacent
     text span or inline object.			
				

