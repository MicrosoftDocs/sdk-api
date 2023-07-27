---
UID: NS:vptype._AMVPDIMINFO
title: AMVPDIMINFO (vptype.h)
description: The AMVPDIMINFO structure specifies the dimensional characteristics of a video port (VP) input stream.
helpviewer_keywords: ["*LPAMVPDIMINFO","AMVPDIMINFO","AMVPDIMINFO structure [DirectShow]","AMVPDIMINFOStructure","LPAMVPDIMINFO","LPAMVPDIMINFO structure pointer [DirectShow]","dshow.amvpdiminfo","vptype/AMVPDIMINFO","vptype/LPAMVPDIMINFO"]
old-location: dshow\amvpdiminfo.htm
tech.root: dshow
ms.assetid: e39cbb85-33f0-4810-aa32-cc96676da123
ms.date: 4/26/2023
ms.keywords: '*LPAMVPDIMINFO, AMVPDIMINFO, AMVPDIMINFO structure [DirectShow], AMVPDIMINFOStructure, LPAMVPDIMINFO, LPAMVPDIMINFO structure pointer [DirectShow], dshow.amvpdiminfo, vptype/AMVPDIMINFO, vptype/LPAMVPDIMINFO'
req.header: vptype.h
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
req.typenames: AMVPDIMINFO, *LPAMVPDIMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMVPDIMINFO
 - vptype/_AMVPDIMINFO
 - LPAMVPDIMINFO
 - vptype/LPAMVPDIMINFO
 - AMVPDIMINFO
 - vptype/AMVPDIMINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVPDIMINFO
---

# AMVPDIMINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVPDIMINFO</b> structure specifies the dimensional characteristics of a video port (VP) input stream.

## -struct-fields

### -field dwFieldWidth

Field width of the data.

### -field dwFieldHeight

Field height of the data.

### -field dwVBIWidth

Width of the VBI data.

### -field dwVBIHeight

Height of the VBI data.

### -field rcValidRegion

Valid rectangle, used for cropping.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>