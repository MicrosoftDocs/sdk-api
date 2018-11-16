---
UID: NE:tvratings.EnTvRat_System
title: EnTvRat_System
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\entvrat_system.htm
tech.root: mstv
ms.assetid: 646927ad-569a-4484-a3ce-6d121210b6be
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Canadian_English, Canadian_French, EnTvRat_System, EnTvRat_System enumeration [Microsoft TV Technologies], MPAA, Reserved4, Reserved7, System5, System6, TvRat_SystemDontKnow, TvRat_kSystems, US_TV, mstv.entvrat_system, tvratings/Canadian_English, tvratings/Canadian_French, tvratings/EnTvRat_System, tvratings/MPAA, tvratings/Reserved4, tvratings/Reserved7, tvratings/System5, tvratings/System6, tvratings/TvRat_SystemDontKnow, tvratings/TvRat_kSystems, tvratings/US_TV
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



This enumeration is used by the <a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat</a> and <a href="https://msdn.microsoft.com/de65e5cd-3f4b-4925-a6b8-636fc2e332ec">IXDSToRat</a> interfaces to define the rating systems being used. When the <a href="https://msdn.microsoft.com/6a67cdb1-9a5c-4130-a29c-05c584702fd9">EvalRat</a> object is initialized, or when the stream changes (such as with a channel change) the default type is <b>TvRat_SystemDontKnow</b>.




## -see-also




<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

