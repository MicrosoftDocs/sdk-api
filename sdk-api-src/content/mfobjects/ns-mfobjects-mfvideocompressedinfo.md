---
UID: NS:mfobjects._MFVideoCompressedInfo
title: MFVideoCompressedInfo (mfobjects.h)
description: Contains information about a video compression format. This structure is used in the MFVIDEOFORMAT structure.
helpviewer_keywords: ["MFVideoCompressedInfo","MFVideoCompressedInfo structure [Media Foundation]","fe9aa287-33e9-4413-8bc5-0e7b2da1112e","mf.mfvideocompressedinfo","mfobjects/MFVideoCompressedInfo"]
old-location: mf\mfvideocompressedinfo.htm
tech.root: mf
ms.assetid: fe9aa287-33e9-4413-8bc5-0e7b2da1112e
ms.date: 12/05/2018
ms.keywords: MFVideoCompressedInfo, MFVideoCompressedInfo structure [Media Foundation], fe9aa287-33e9-4413-8bc5-0e7b2da1112e, mf.mfvideocompressedinfo, mfobjects/MFVideoCompressedInfo
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFVideoCompressedInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoCompressedInfo
 - mfobjects/_MFVideoCompressedInfo
 - MFVideoCompressedInfo
 - mfobjects/MFVideoCompressedInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFVideoCompressedInfo
---

# MFVideoCompressedInfo structure


## -description

Contains information about a video compression format. This structure is used in the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -struct-fields

### -field AvgBitrate

Average bit rate of the encoded video stream, in bits per second.

### -field AvgBitErrorRate

Expected error rate, in bits per second.

### -field MaxKeyFrameSpacing

Number of frames between key frames.

## -remarks

For uncompressed video formats, set the structure members to zero.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>