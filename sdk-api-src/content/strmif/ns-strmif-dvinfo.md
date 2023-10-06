---
UID: NS:strmif.DVINFO
title: DVINFO (strmif.h)
description: The DVINFO structure describes the format of a digital video (DV) stream.
helpviewer_keywords: ["*PDVINFO","DVINFO","DVINFO structure [DirectShow]","DVINFOStructure","PDVINFO","PDVINFO structure pointer [DirectShow]","dshow.dvinfo","strmif/DVINFO","strmif/PDVINFO"]
old-location: dshow\dvinfo.htm
tech.root: dshow
ms.assetid: 285a56fc-9c25-4c5a-ae6a-146c17b00e84
ms.date: 4/26/2023
ms.keywords: '*PDVINFO, DVINFO, DVINFO structure [DirectShow], DVINFOStructure, PDVINFO, PDVINFO structure pointer [DirectShow], dshow.dvinfo, strmif/DVINFO, strmif/PDVINFO'
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: DVINFO, *PDVINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DVINFO
 - strmif/DVINFO
 - PDVINFO
 - strmif/PDVINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVINFO
---

# DVINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DVINFO</b> structure describes the format of a digital video (DV) stream.

## -struct-fields

### -field dwDVAAuxSrc

Specifies the audio auxiliary (AAUX) source pack for the first audio block.

### -field dwDVAAuxCtl

Specifies the AAUX source control Pack for the first audio block.

### -field dwDVAAuxSrc1

Specifies the AAUX source pack for the second audio block.

### -field dwDVAAuxCtl1

Specifies the AAUX source control pack for the second audio block.

### -field dwDVVAuxSrc

Specifies the video auxiliary (VAUX) source pack.

### -field dwDVVAuxCtl

Specifies the VAUX source control pack.

### -field dwDVReserved

Reserved. Set this array to zero.

## -remarks

The AAUX and VAUX packs are defined in IEC 61834-4.

## -see-also

<a href="/windows/desktop/DirectShow/dv-data-in-the-avi-file-format">DV Data in the AVI File Format</a>



<a href="/windows/desktop/DirectShow/dvinfo-field-settings-in-the-msdv-driver">DVINFO Field Settings in the MSDV Driver</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>