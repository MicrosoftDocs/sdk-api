---
UID: NS:mfobjects._MFVideoSurfaceInfo
title: MFVideoSurfaceInfo (mfobjects.h)
description: Contains information about an uncompressed video format. This structure is used in the MFVIDEOFORMAT structure.
helpviewer_keywords: ["MFVideoSurfaceInfo","MFVideoSurfaceInfo structure [Media Foundation]","b48099a2-8427-496c-9a60-ace5b89d81e9","mf.mfvideosurfaceinfo","mfobjects/MFVideoSurfaceInfo"]
old-location: mf\mfvideosurfaceinfo.htm
tech.root: mf
ms.assetid: b48099a2-8427-496c-9a60-ace5b89d81e9
ms.date: 12/05/2018
ms.keywords: MFVideoSurfaceInfo, MFVideoSurfaceInfo structure [Media Foundation], b48099a2-8427-496c-9a60-ace5b89d81e9, mf.mfvideosurfaceinfo, mfobjects/MFVideoSurfaceInfo
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
req.typenames: MFVideoSurfaceInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoSurfaceInfo
 - mfobjects/_MFVideoSurfaceInfo
 - MFVideoSurfaceInfo
 - mfobjects/MFVideoSurfaceInfo
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
 - MFVideoSurfaceInfo
---

# MFVideoSurfaceInfo structure


## -description

Contains information about an uncompressed video format. This structure is used in the <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat">MFVIDEOFORMAT</a> structure.

## -struct-fields

### -field Format

For compressed formats, this value must be zero. For uncompressed formats, the value is a FOURCC or <b>D3DFORMAT</b> value that identifies the format. Use the <b>Data1</b> field from the subtype GUID. See <a href="/windows/desktop/medfound/video-subtype-guids">Video Subtype GUIDs</a>.

### -field PaletteEntries

Number of palette entries. The value must be between 0 and 256.

### -field Palette

Array of <a href="/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry">MFPaletteEntry Union</a>s that contains the color table for a palettized format. The size of the array is given in the <b>PaletteEntries</b> member. If the format is not palettized, set <b>PaletteEntries</b> to zero.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>