---
UID: NE:tvratings.BfEnTvRat_Attributes_US_TV
title: BfEnTvRat_Attributes_US_TV
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\bfentvrat_attributes_us_tv.htm
tech.root: mstv
ms.assetid: 3ad1736f-d27f-4aba-ab68-e7aca407d182
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BfEnTvRat_Attributes_US_TV, BfEnTvRat_Attributes_US_TV enumeration [Microsoft TV Technologies], US_TV_IsAdultLanguage, US_TV_IsBlocked, US_TV_IsSexualSituation, US_TV_IsSexuallySuggestiveDialog, US_TV_IsViolent, US_TV_ValidAttrSubmask, mstv.bfentvrat_attributes_us_tv, tvratings/BfEnTvRat_Attributes_US_TV, tvratings/US_TV_IsAdultLanguage, tvratings/US_TV_IsBlocked, tvratings/US_TV_IsSexualSituation, tvratings/US_TV_IsSexuallySuggestiveDialog, tvratings/US_TV_IsViolent, tvratings/US_TV_ValidAttrSubmask
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
 - BfEnTvRat_Attributes_US_TV
product: Windows
targetos: Windows
req.typenames: BfEnTvRat_Attributes_US_TV
req.redist: 
---

# BfEnTvRat_Attributes_US_TV enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>BfEnTvRat_Attributes_US_TV</b> enumeration type specifies content rating attributes in the US television system.


## -enum-fields




### -field US_TV_IsBlocked

Block playback.


### -field US_TV_IsViolent

Content contains violence.


### -field US_TV_IsSexualSituation

Content contains sexual situations.


### -field US_TV_IsAdultLanguage

Content contains adult language.


### -field US_TV_IsSexuallySuggestiveDialog

Content contains sexually suggestive dialogue.


### -field US_TV_ValidAttrSubmask

A bitmask of all valid attribute bits for the US TV ratings system.


## -remarks



This enumeration type maps <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> flags to the MPAA rating system.




## -see-also




<a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a>



<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

