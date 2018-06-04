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

# _IMAPI_READ_TRACK_ADDRESS_TYPE enumeration


## -description


Defines values that indicate how to interpret track addresses for the current disc profile of a randomly-writable, hardware-defect-managed media type.


## -enum-fields




### -field IMAPI_READ_TRACK_ADDRESS_TYPE_LBA

Interpret the address field as an LBA (sector address).  The returned data should reflect the information for the track which contains the specified LBA.


### -field IMAPI_READ_TRACK_ADDRESS_TYPE_TRACK

Interpret the address field as a track number.  The returned data should reflect the information for the specified track.  This version of the command has the greatest compatibility with legacy devices.


### -field IMAPI_READ_TRACK_ADDRESS_TYPE_SESSION

Interpret the address field as a session number.  The returned data should reflect the information for the first track which exists in the specified session.  Note that not all drives support this method.

