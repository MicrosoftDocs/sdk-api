---
UID: NS:mfobjects._MFVIDEOFORMAT
title: MFVIDEOFORMAT (mfobjects.h)
description: Describes a video format.
helpviewer_keywords: ["7fbc4a35-117c-4f0c-9e9b-ff44e30a1618","MFVIDEOFORMAT","MFVIDEOFORMAT structure [Media Foundation]","mf.mfvideoformat","mfobjects/MFVIDEOFORMAT"]
old-location: mf\mfvideoformat.htm
tech.root: mf
ms.assetid: 7fbc4a35-117c-4f0c-9e9b-ff44e30a1618
ms.date: 12/05/2018
ms.keywords: 7fbc4a35-117c-4f0c-9e9b-ff44e30a1618, MFVIDEOFORMAT, MFVIDEOFORMAT structure [Media Foundation], mf.mfvideoformat, mfobjects/MFVIDEOFORMAT
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
req.typenames: MFVIDEOFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVIDEOFORMAT
 - mfobjects/_MFVIDEOFORMAT
 - MFVIDEOFORMAT
 - mfobjects/MFVIDEOFORMAT
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
 - MFVIDEOFORMAT
---

# MFVIDEOFORMAT structure


## -description

Describes a video format.

## -struct-fields

### -field dwSize

Size of the structure, in bytes. This value includes the size of the palette entries that may appear after the <b>surfaceInfo</b> member.

### -field videoInfo

<a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo">MFVideoInfo</a> structure. This structure contains information that applies to both compressed and uncompressed formats.

### -field guidFormat

Video subtype. See <a href="/windows/desktop/medfound/video-subtype-guids">Video Subtype GUIDs</a>.

### -field compressedInfo

<a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideocompressedinfo">MFVideoCompressedInfo</a> structure. This structure contains information that applies only to compressed formats.

### -field surfaceInfo

<a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideosurfaceinfo">MFVideoSurfaceInfo</a> structure. This structure contains information that applies only to uncompressed formats.

## -remarks

Applications should avoid using this structure. Instead, it is recommended that applications use attributes to describe the video format. For a list of media type attributes, see <a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>. With attributes, you can set just the format information that you know, which is easier (and more likely to be accurate) than trying to fill in complete format information for the <b>MFVIDEOFORMAT</b> structure.

To initialize a media type object from an <b>MFVIDEOFORMAT</b> structure, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat">MFInitMediaTypeFromMFVideoFormat</a>.

You can use the <b>MFVIDEOFORMAT</b> structure as the format block for a DirectShow media type. Set the format GUID to FORMAT_MFVideoFormat.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>