---
UID: NE:mfobjects._MFVideoTransferMatrix
title: MFVideoTransferMatrix (mfobjects.h)
description: Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'.
helpviewer_keywords: ["08a05ee8-b053-4480-b7f9-6d96e541ccd9","MFVideoTransferMatrix","MFVideoTransferMatrix enumeration [Media Foundation]","MFVideoTransferMatrix_BT601","MFVideoTransferMatrix_BT709","MFVideoTransferMatrix_ForceDWORD","MFVideoTransferMatrix_Last","MFVideoTransferMatrix_SMPTE240M","MFVideoTransferMatrix_Unknown","mf.mfvideotransfermatrix","mfobjects/MFVideoTransferMatrix","mfobjects/MFVideoTransferMatrix_BT601","mfobjects/MFVideoTransferMatrix_BT709","mfobjects/MFVideoTransferMatrix_ForceDWORD","mfobjects/MFVideoTransferMatrix_Last","mfobjects/MFVideoTransferMatrix_SMPTE240M","mfobjects/MFVideoTransferMatrix_Unknown"]
old-location: mf\mfvideotransfermatrix.htm
tech.root: mf
ms.assetid: 08a05ee8-b053-4480-b7f9-6d96e541ccd9
ms.date: 12/05/2018
ms.keywords: 08a05ee8-b053-4480-b7f9-6d96e541ccd9, MFVideoTransferMatrix, MFVideoTransferMatrix enumeration [Media Foundation], MFVideoTransferMatrix_BT601, MFVideoTransferMatrix_BT709, MFVideoTransferMatrix_ForceDWORD, MFVideoTransferMatrix_Last, MFVideoTransferMatrix_SMPTE240M, MFVideoTransferMatrix_Unknown, mf.mfvideotransfermatrix, mfobjects/MFVideoTransferMatrix, mfobjects/MFVideoTransferMatrix_BT601, mfobjects/MFVideoTransferMatrix_BT709, mfobjects/MFVideoTransferMatrix_ForceDWORD, mfobjects/MFVideoTransferMatrix_Last, mfobjects/MFVideoTransferMatrix_SMPTE240M, mfobjects/MFVideoTransferMatrix_Unknown
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
req.typenames: MFVideoTransferMatrix
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoTransferMatrix
 - mfobjects/_MFVideoTransferMatrix
 - MFVideoTransferMatrix
 - mfobjects/MFVideoTransferMatrix
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
 - MFVideoTransferMatrix
---

# MFVideoTransferMatrix enumeration


## -description

Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'.

## -enum-fields

### -field MFVideoTransferMatrix_Unknown:0

Unknown transfer matrix. Treat as MFVideoTransferMatrix_BT709.

### -field MFVideoTransferMatrix_BT709:1

ITU-R BT.709 transfer matrix.

### -field MFVideoTransferMatrix_BT601:2

ITU-R BT.601 transfer matrix. Also used for SMPTE 170 and ITU-R BT.470-2 System B,G.

### -field MFVideoTransferMatrix_SMPTE240M:3

SMPTE 240M transfer matrix.

### -field MFVideoTransferMatrix_BT2020_10:4

### -field MFVideoTransferMatrix_BT2020_12:5

### -field MFVideoTransferMatrix_Last

Reserved.

### -field MFVideoTransferMatrix_ForceDWORD:0x7fffffff

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mf-mt-yuv-matrix-attribute">MF_MT_YUV_MATRIX</a> attribute.

For more information about these values, see the remarks for the <a href="/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_videotransfermatrix">DXVA2_VideoTransferMatrix</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.

## -see-also

<a href="/windows/desktop/medfound/extended-color-information">Extended Color Information</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/video-media-types">Video Media Types</a>
