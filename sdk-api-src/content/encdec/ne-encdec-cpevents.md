---
UID: NE:encdec.CPEvents
title: CPEvents
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\cpevents.htm
old-project: mstv
ms.assetid: 7a8ef55f-0546-4642-960d-6bd6093ab5d2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CPEVENT_COPP, CPEVENT_DOWNRES, CPEVENT_LICENSE, CPEVENT_NONE, CPEVENT_RATINGS, CPEVENT_ROLLBACK, CPEVENT_SAC, CPEVENT_STUBLIB, CPEVENT_UNTRUSTEDGRAPH, CPEvents, CPEvents enumeration [Microsoft TV Technologies], encdec/CPEVENT_COPP, encdec/CPEVENT_DOWNRES, encdec/CPEVENT_LICENSE, encdec/CPEVENT_NONE, encdec/CPEVENT_RATINGS, encdec/CPEVENT_ROLLBACK, encdec/CPEVENT_SAC, encdec/CPEVENT_STUBLIB, encdec/CPEVENT_UNTRUSTEDGRAPH, encdec/CPEvents, mstv.cpevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: encdec.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CPEvents
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EncDec.h
api_name:
 - CPEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

