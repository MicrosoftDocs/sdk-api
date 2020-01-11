---
UID: NS:mfapi.tagCapturedMetadataExposureCompensation
title: CapturedMetadataExposureCompensation (mfapi.h)
description: This structure contains blob information for the EV compensation feedback for the photo captured.
old-location: stream\capturedmetadataexposurecompensation.htm
tech.root: stream
ms.assetid: B7C32495-F9A1-4206-81D2-DCA247F83901
ms.date: 12/05/2018
ms.keywords: CapturedMetadataExposureCompensation, CapturedMetadataExposureCompensation structure [Streaming Media Devices], mfapi/CapturedMetadataExposureCompensation, stream.capturedmetadataexposurecompensation
f1_keywords:
- mfapi/CapturedMetadataExposureCompensation
dev_langs:
- c++
req.header: mfapi.h
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
- Mfapi.h
api_name:
- CapturedMetadataExposureCompensation
targetos: Windows
req.typenames: CapturedMetadataExposureCompensation
req.redist: 
ms.custom: 19H1
---

# CapturedMetadataExposureCompensation structure


## -description


This structure contains blob information for the EV compensation feedback for the photo captured.


## -struct-fields




### -field Flags

A KSCAMERA_EXTENDEDPROP_EVCOMP_XXX step flag.


### -field Value

The EV compensation value in units of the step specified.

