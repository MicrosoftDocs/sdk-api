---
UID: NE:tvratings.BfEnTvRat_Attributes_MPAA
title: BfEnTvRat_Attributes_MPAA (tvratings.h)
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\bfentvrat_attributes_mpaa.htm
tech.root: mstv
ms.assetid: 520046a3-2542-409e-9d8f-91a91cad54f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BfEnTvRat_Attributes_MPAA, BfEnTvRat_Attributes_MPAA enumeration [Microsoft TV Technologies], MPAA_IsBlocked, MPAA_ValidAttrSubmask, mstv.bfentvrat_attributes_mpaa, tvratings/BfEnTvRat_Attributes_MPAA, tvratings/MPAA_IsBlocked, tvratings/MPAA_ValidAttrSubmask
ms.topic: enum
f1_keywords: ["tvratings/BfEnTvRat_Attributes_MPAA"]
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tvratings.h
api_name:
 - BfEnTvRat_Attributes_MPAA
product: Windows
targetos: Windows
req.typenames: BfEnTvRat_Attributes_MPAA
req.redist: 
ms.custom: 19H1
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



This enumeration type maps <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-bfentvrat_genericattributes">BfEnTvRat_GenericAttributes</a> flags to the MPAA rating system. The only valid flag is MPAA_IsBlocked.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-enumerations">TV Ratings Enumerations</a>
 

 

