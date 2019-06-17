---
UID: NE:tvratings.EnTvRat_System
title: EnTvRat_System (tvratings.h)
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\entvrat_system.htm
tech.root: mstv
ms.assetid: 646927ad-569a-4484-a3ce-6d121210b6be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Canadian_English, Canadian_French, EnTvRat_System, EnTvRat_System enumeration [Microsoft TV Technologies], MPAA, Reserved4, Reserved7, System5, System6, TvRat_SystemDontKnow, TvRat_kSystems, US_TV, mstv.entvrat_system, tvratings/Canadian_English, tvratings/Canadian_French, tvratings/EnTvRat_System, tvratings/MPAA, tvratings/Reserved4, tvratings/Reserved7, tvratings/System5, tvratings/System6, tvratings/TvRat_SystemDontKnow, tvratings/TvRat_kSystems, tvratings/US_TV
ms.topic: enum
f1_keywords: ["tvratings/EnTvRat_System"]
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
 - EnTvRat_System
product: Windows
targetos: Windows
req.typenames: EnTvRat_System
req.redist: 
ms.custom: 19H1
---

# EnTvRat_System enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>EnTvRat_System</b> enumeration type specifies the rating system in use.


## -enum-fields




### -field MPAA

MPAA rating system.


### -field US_TV

US rating system.


### -field Canadian_English

English-Canadian rating system.


### -field Canadian_French

French-Canadian rating system.


### -field Reserved4

Not used.


### -field System5

System 5 in XDS rating table 19 (reserved for non–North American systems).


### -field System6

System 6 in XDS rating table 19 (reserved for non–North American systems).


### -field Reserved7

Not used.


### -field PBDA


### -field AgeBased


### -field TvRat_kSystems

Specifies the number of rating systems that can be defined.


### -field TvRat_SystemDontKnow

System currently unknown. This value is used after channel changes or other stream discontinuities, until a valid rating is obtained from the stream.


## -remarks



This enumeration is used by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ievalrat">IEvalRat</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ixdstorat">IXDSToRat</a> interfaces to define the rating systems being used. When the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/evalrat-object">EvalRat</a> object is initialized, or when the stream changes (such as with a channel change) the default type is <b>TvRat_SystemDontKnow</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-enumerations">TV Ratings Enumerations</a>
 

 

