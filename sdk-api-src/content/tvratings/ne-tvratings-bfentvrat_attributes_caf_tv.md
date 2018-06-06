---
UID: NE:tvratings.BfEnTvRat_Attributes_CAF_TV
title: BfEnTvRat_Attributes_CAF_TV
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\bfentvrat_attributes_caf_tv.htm
old-project: mstv
ms.assetid: f6d10852-f28e-492e-9687-d09cd132d06e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: BfEnTvRat_Attributes_CAF_TV, BfEnTvRat_Attributes_CAF_TV enumeration [Microsoft TV Technologies], CAF_IsBlocked, CAF_ValidAttrSubmask, mstv.bfentvrat_attributes_caf_tv, tvratings/BfEnTvRat_Attributes_CAF_TV, tvratings/CAF_IsBlocked, tvratings/CAF_ValidAttrSubmask
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BfEnTvRat_Attributes_CAF_TV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tvratings.h
api_name:
 - BfEnTvRat_Attributes_CAF_TV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# BfEnTvRat_Attributes_CAF_TV enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>BfEnTvRat_Attributes_CAF_TV</b> enumeration type specifies content rating attributes in the French-Canadian television system.


## -enum-fields




### -field CAF_IsBlocked

Block playback.


### -field CAF_ValidAttrSubmask

A bitmask of all valid attribute bits for the French-Canadian rating system.


## -remarks



This enumeration type maps <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> flags to the French-Canadian television system. The only valid flag is CAF_IsBlocked.




## -see-also




<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

