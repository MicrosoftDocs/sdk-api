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

# _IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration


## -description


Defines the digital copy setting values available for a given track.


## -enum-fields




### -field IMAPI_CD_TRACK_DIGITAL_COPY_PERMITTED

Digital copies of the given track are allowed.


### -field IMAPI_CD_TRACK_DIGITAL_COPY_PROHIBITED

Digital copies of the given track are not allowed using consumer electronics CD recorders.  This condition typically has no effect on PC-based CD players.


### -field IMAPI_CD_TRACK_DIGITAL_COPY_SCMS

The given track is a digital copy of a copy protected track.  No further copies using consumer electronics CD recorders will be allowed.  This condition typically has no effect on PC-based CD players.

