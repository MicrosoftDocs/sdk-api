---
UID: NS:mfapi.tagMetadataTimeStamps
title: MetadataTimeStamps (mfapi.h)
description: The MetadataTimeStamps structure describes the blob format for the MF_CAPTURE_METADATA_FACEROITIMESTAMPS attribute.
helpviewer_keywords: ["MetadataTimeStamps","MetadataTimeStamps structure [Streaming Media Devices]","mfapi/MetadataTimeStamps","stream.metadatatimestamps"]
old-location: stream\metadatatimestamps.htm
tech.root: stream
ms.assetid: F7E5349B-37F0-4B94-B42B-EAEB04DC1AB5
ms.date: 12/05/2018
ms.keywords: MetadataTimeStamps, MetadataTimeStamps structure [Streaming Media Devices], mfapi/MetadataTimeStamps, stream.metadatatimestamps
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
targetos: Windows
req.typenames: MetadataTimeStamps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMetadataTimeStamps
 - mfapi/tagMetadataTimeStamps
 - MetadataTimeStamps
 - mfapi/MetadataTimeStamps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MetadataTimeStamps
---

# MetadataTimeStamps structure


## -description

The <b>MetadataTimeStamps</b> structure describes the blob format for the <b>MF_CAPTURE_METADATA_FACEROITIMESTAMPS</b> attribute.

## -struct-fields

### -field Flags

Bitwise OR of the <b>MF_METADATATIMESTAMPS_*</b> flags.

### -field Device

QPC time for the sample  the face rectangle is derived from (in 100ns).

### -field Presentation

PTS for the sample  the face rectangle is derived from (in 100ns).

## -remarks

The <b>MF_CAPTURE_METADATA_FACEROITIMESTAMPS</b> attribute contains the time stamp information for the face ROIs identified in <b>MF_CAPTURE_METADATA_FACEROIS</b>.  For a  device that cannot provide the time stamp for face ROIs, this attribute should be omitted.

For the <b>Flags</b> field, the following bit flags  indicate which time stamp is valid:


```
#define MF_METADATATIMESTAMPS_DEVICE        0x00000001
#define MF_METADATATIMESTAMPS_PRESENTATION  0x00000002
```


MFT0 must set <b>Flags</b> to <b>MF_METADATATIEMSTAMPS_DEVICE</b> and the appropriate QPC time for <b>Device</b>, if the driver provides the timestamp metadata for the face ROIs.

The <b>MetadataTimeStamps</b> structure only describes the blob format for the <b>MF_CAPTURE_METADATA_FACEROITIMESTAMPS</b> attribute.  The metadata item structure for timestamp (<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader">KSCAMERA_METADATA_ITEMHEADER</a> + timestamp metadata payload) is up to driver and must be 8-byte aligned.