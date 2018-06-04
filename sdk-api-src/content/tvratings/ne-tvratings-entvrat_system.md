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
 

 

