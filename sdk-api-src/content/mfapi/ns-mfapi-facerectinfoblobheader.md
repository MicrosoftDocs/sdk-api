---
UID: NS:mfapi.tagFaceRectInfoBlobHeader
title: FaceRectInfoBlobHeader (mfapi.h)
description: The FaceRectInfoBlobHeader structure describes the size and count information of the blob format for the MF_CAPTURE_METADATA_FACEROIS attribute.
helpviewer_keywords: ["FaceRectInfoBlobHeader","FaceRectInfoBlobHeader structure [Streaming Media Devices]","mfapi/FaceRectInfoBlobHeader","stream.facerectinfoblobheader"]
old-location: stream\facerectinfoblobheader.htm
tech.root: stream
ms.assetid: BDDC33C2-CD2D-4F97-AAD1-DF69250F60B3
ms.date: 12/05/2018
ms.keywords: FaceRectInfoBlobHeader, FaceRectInfoBlobHeader structure [Streaming Media Devices], mfapi/FaceRectInfoBlobHeader, stream.facerectinfoblobheader
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
req.typenames: FaceRectInfoBlobHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFaceRectInfoBlobHeader
 - mfapi/tagFaceRectInfoBlobHeader
 - FaceRectInfoBlobHeader
 - mfapi/FaceRectInfoBlobHeader
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
 - FaceRectInfoBlobHeader
---

# FaceRectInfoBlobHeader structure


## -description

The <b>FaceRectInfoBlobHeader</b> structure describes the size and count information of the blob format for the <b>MF_CAPTURE_METADATA_FACEROIS</b> attribute.

## -struct-fields

### -field Size

Size of this header + all following <a href="/windows/desktop/api/mfapi/ns-mfapi-facerectinfo">FaceRectInfo</a> structures.

### -field Count

Number of <b>FaceRectInfo</b> structures in the blob.