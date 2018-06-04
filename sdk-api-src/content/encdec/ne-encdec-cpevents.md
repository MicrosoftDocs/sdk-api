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

# CPEvents enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>CPEvents</b> enumeration defines copy protection events for the Decrypter/Detagger filter. This enumeration is used with the EVENTID_EncDecFilterEvent event. For more information, see <a href="https://msdn.microsoft.com/73a6a4fd-cca2-4143-91f9-37f4f6d952b8">TV Ratings Broadcast Events</a>.


## -enum-fields




### -field CPEVENT_NONE

No content protection issues.


### -field CPEVENT_RATINGS

Content is blocked because of parental ratings.


### -field CPEVENT_COPP

Content is blocked because of copy protection rules.


### -field CPEVENT_LICENSE

Content is blocked because the DRM license is not valid.


### -field CPEVENT_ROLLBACK

Content is blocked because the system detected that the clock was rolled back.


### -field CPEVENT_SAC

Content is blocked because the filter graph contains untrusted components.


### -field CPEVENT_DOWNRES

Content is being rendered at a lower resolution due to copy protection.


### -field CPEVENT_STUBLIB

Content is blocked because the filter graph contains untrusted components.


### -field CPEVENT_UNTRUSTEDGRAPH

Content is blocked because the filter graph contains untrusted components.


### -field CPEVENT_PROTECTWINDOWED




## -see-also




<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 

