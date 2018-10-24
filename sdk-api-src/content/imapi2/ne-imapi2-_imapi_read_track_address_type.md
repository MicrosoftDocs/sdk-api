---
UID: NE:imapi2._IMAPI_READ_TRACK_ADDRESS_TYPE
title: "_IMAPI_READ_TRACK_ADDRESS_TYPE"
author: windows-sdk-content
description: Defines values that indicate how to interpret track addresses for the current disc profile of a randomly-writable, hardware-defect-managed media type.
old-location: imapi\imapi_read_track_address_type.htm
tech.root: imapi
ms.assetid: 228bcc7b-603f-420d-a8a9-cde5b0bbf2e3
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PIMAPI_READ_TRACK_ADDRESS_TYPE, IMAPI_READ_TRACK_ADDRESS_TYPE, IMAPI_READ_TRACK_ADDRESS_TYPE enumeration [IMAPI], IMAPI_READ_TRACK_ADDRESS_TYPE_LBA, IMAPI_READ_TRACK_ADDRESS_TYPE_SESSION, IMAPI_READ_TRACK_ADDRESS_TYPE_TRACK, PIMAPI_READ_TRACK_ADDRESS_TYPE, PIMAPI_READ_TRACK_ADDRESS_TYPE enumeration pointer [IMAPI], _IMAPI_READ_TRACK_ADDRESS_TYPE, imapi.imapi_read_track_address_type, imapi2/IMAPI_READ_TRACK_ADDRESS_TYPE, imapi2/IMAPI_READ_TRACK_ADDRESS_TYPE_LBA, imapi2/IMAPI_READ_TRACK_ADDRESS_TYPE_SESSION, imapi2/IMAPI_READ_TRACK_ADDRESS_TYPE_TRACK, imapi2/PIMAPI_READ_TRACK_ADDRESS_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IMAPI_READ_TRACK_ADDRESS_TYPE
product: Windows
targetos: Windows
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
req.redist: 
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

