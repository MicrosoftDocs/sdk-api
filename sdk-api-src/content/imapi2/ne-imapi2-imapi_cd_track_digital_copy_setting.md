---
UID: NE:imapi2._IMAPI_CD_TRACK_DIGITAL_COPY_SETTING
title: IMAPI_CD_TRACK_DIGITAL_COPY_SETTING (imapi2.h)
author: windows-sdk-content
description: Defines the digital copy setting values available for a given track.
old-location: imapi\imapi_cd_track_digital_copy_setting.htm
tech.root: imapi
ms.assetid: 6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIMAPI_CD_TRACK_DIGITAL_COPY_SETTING, IMAPI_CD_TRACK_DIGITAL_COPY_PERMITTED, IMAPI_CD_TRACK_DIGITAL_COPY_PROHIBITED, IMAPI_CD_TRACK_DIGITAL_COPY_SCMS, IMAPI_CD_TRACK_DIGITAL_COPY_SETTING, IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration [IMAPI], imapi.imapi_cd_track_digital_copy_setting, imapi2/IMAPI_CD_TRACK_DIGITAL_COPY_PERMITTED, imapi2/IMAPI_CD_TRACK_DIGITAL_COPY_PROHIBITED, imapi2/IMAPI_CD_TRACK_DIGITAL_COPY_SCMS, imapi2/IMAPI_CD_TRACK_DIGITAL_COPY_SETTING"
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
 - IMAPI_CD_TRACK_DIGITAL_COPY_SETTING
product: Windows
targetos: Windows
req.typenames: IMAPI_CD_TRACK_DIGITAL_COPY_SETTING, *PIMAPI_CD_TRACK_DIGITAL_COPY_SETTING
req.redist: 
---

# IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration


## -description


Defines the digital copy setting values available for a given track.


## -enum-fields




### -field IMAPI_CD_TRACK_DIGITAL_COPY_PERMITTED

Digital copies of the given track are allowed.


### -field IMAPI_CD_TRACK_DIGITAL_COPY_PROHIBITED

Digital copies of the given track are not allowed using consumer electronics CD recorders.  This condition typically has no effect on PC-based CD players.


### -field IMAPI_CD_TRACK_DIGITAL_COPY_SCMS

The given track is a digital copy of a copy protected track.  No further copies using consumer electronics CD recorders will be allowed.  This condition typically has no effect on PC-based CD players.

