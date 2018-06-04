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
 

 

