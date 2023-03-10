---
UID: NS:mfapi.tagFaceCharacterization
title: FaceCharacterization (mfapi.h)
description: The FaceCharacterization structure describes the blob format for the MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS attribute.
helpviewer_keywords: ["FaceCharacterization","FaceCharacterization structure [Streaming Media Devices]","mfapi/FaceCharacterization","stream.facecharacterization"]
old-location: stream\facecharacterization.htm
tech.root: stream
ms.assetid: 8A8F6E06-DA09-4595-BF42-8B905453CCCA
ms.date: 12/05/2018
ms.keywords: FaceCharacterization, FaceCharacterization structure [Streaming Media Devices], mfapi/FaceCharacterization, stream.facecharacterization
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
req.typenames: FaceCharacterization
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFaceCharacterization
 - mfapi/tagFaceCharacterization
 - FaceCharacterization
 - mfapi/FaceCharacterization
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
 - FaceCharacterization
---

# FaceCharacterization structure


## -description

The <b>FaceCharacterization</b> structure describes the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.

## -struct-fields

### -field BlinkScoreLeft

0 indicates no blink for the left eye, 100 indicates definite blink for the left eye (0 - 100).

### -field BlinkScoreRight

0 indicates no blink for the right eye, 100 indicates definite blink for the right eye (0 - 100).

### -field FacialExpression

A  defined facial expression value.

### -field FacialExpressionScore

0 indicates no such facial expression as identified, 100 indicates definite such facial expression as defined (0 - 100).

## -remarks

The <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute contains the blink and facial expression state for the face ROIs identified in <b>MF_CAPTURE_METADATA_FACEROIS</b>.  For a  device that does not support blink or facial expression detection, this attribute should be omitted.

The facial expressions that can be detected are defined as follows:


```
#define MF_METADATAFACIALEXPRESSION_SMILE             0x00000001
```


The <a href="/windows/desktop/api/mfapi/ns-mfapi-facecharacterizationblobheader">FaceCharacterizationBlobHeader</a> and <b>FaceCharacterization</b> structures only describe the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.  The metadata item structure for the face characterizations (<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader">KSCAMERA_METADATA_ITEMHEADER</a> + face characterizations metadata payload) is up to driver and must be 8-byte aligned.