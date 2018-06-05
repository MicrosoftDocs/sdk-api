---
UID: NE:dwrite.DWRITE_BREAK_CONDITION
title: DWRITE_BREAK_CONDITION
author: windows-sdk-content
description: Indicates the condition at the edges of inline object or text used to determine line-breaking behavior.
old-location: directwrite\dwrite_break_condition.htm
old-project: DirectWrite
ms.assetid: 26dbe63e-eeee-486f-aa94-74320b190fcb
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DWRITE_BREAK_CONDITION, DWRITE_BREAK_CONDITION enumeration [Direct Write], DWRITE_BREAK_CONDITION_CAN_BREAK, DWRITE_BREAK_CONDITION_MAY_NOT_BREAK, DWRITE_BREAK_CONDITION_MUST_BREAK, DWRITE_BREAK_CONDITION_NEUTRAL, directwrite.dwrite_break_condition, dwrite/DWRITE_BREAK_CONDITION, dwrite/DWRITE_BREAK_CONDITION_CAN_BREAK, dwrite/DWRITE_BREAK_CONDITION_MAY_NOT_BREAK, dwrite/DWRITE_BREAK_CONDITION_MUST_BREAK, dwrite/DWRITE_BREAK_CONDITION_NEUTRAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dwrite.h
api_name:
-	DWRITE_BREAK_CONDITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
				

