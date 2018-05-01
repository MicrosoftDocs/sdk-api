---
UID: NE:tvratings.BfEnTvRat_Attributes_MPAA
title: BfEnTvRat_Attributes_MPAA
author: windows-driver-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\bfentvrat_attributes_mpaa.htm
old-project: mstv
ms.assetid: 520046a3-2542-409e-9d8f-91a91cad54f3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: BfEnTvRat_Attributes_MPAA, BfEnTvRat_Attributes_MPAA enumeration [Microsoft TV Technologies], MPAA_IsBlocked, MPAA_ValidAttrSubmask, mstv.bfentvrat_attributes_mpaa, tvratings/BfEnTvRat_Attributes_MPAA, tvratings/MPAA_IsBlocked, tvratings/MPAA_ValidAttrSubmask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BfEnTvRat_Attributes_MPAA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tvratings.h
api_name:
-	BfEnTvRat_Attributes_MPAA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# BfEnTvRat_Attributes_MPAA enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>BfEnTvRat_Attributes_MPAA</b> enumeration type specifies content rating attributes in the Motion Picture Association of America (MPAA) rating system.


## -enum-fields




### -field MPAA_IsBlocked

Block playback.


### -field MPAA_ValidAttrSubmask

A bitmask of all valid attribute bits for the MPAA rating system.


## -remarks



This enumeration type maps <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> flags to the MPAA rating system. The only valid flag is MPAA_IsBlocked.




## -see-also




<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

