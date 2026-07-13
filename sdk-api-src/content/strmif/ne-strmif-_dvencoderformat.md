---
UID: NE:strmif._DVENCODERFORMAT
title: "_DVENCODERFORMAT (strmif.h)"
description: Indicates the digital video (DV) format.
helpviewer_keywords: ["DVENCODERFORMAT","DVENCODERFORMATEnumeration","DVENCODERFORMAT_DVHD","DVENCODERFORMAT_DVSD","DVENCODERFORMAT_DVSL","_DVENCODERFORMAT","_DVENCODERFORMAT enumeration [DirectShow]","dshow.dvencoderformat","strmif/DVENCODERFORMAT_DVHD","strmif/DVENCODERFORMAT_DVSD","strmif/DVENCODERFORMAT_DVSL","strmif/_DVENCODERFORMAT"]
old-location: dshow\dvencoderformat.htm
tech.root: dshow
ms.assetid: 462c8034-5931-435d-8f18-b58842f2e234
ms.date: 4/26/2023
ms.keywords: DVENCODERFORMAT, DVENCODERFORMATEnumeration, DVENCODERFORMAT_DVHD, DVENCODERFORMAT_DVSD, DVENCODERFORMAT_DVSL, _DVENCODERFORMAT, _DVENCODERFORMAT enumeration [DirectShow], dshow.dvencoderformat, strmif/DVENCODERFORMAT_DVHD, strmif/DVENCODERFORMAT_DVSD, strmif/DVENCODERFORMAT_DVSL, strmif/_DVENCODERFORMAT
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DVENCODERFORMAT
 - strmif/_DVENCODERFORMAT
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
 - _DVENCODERFORMAT
---

# _DVENCODERFORMAT enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates the digital video (DV) format.

## -enum-fields

### -field DVENCODERFORMAT_DVSD:2007

Use the 'dvsd' stream handler.

### -field DVENCODERFORMAT_DVHD:2008

Use the 'dvhd' stream handler.

### -field DVENCODERFORMAT_DVSL:2009

Use the 'dvsl' stream handler.

## -remarks

This enumeration specifies the <b>fccType</b> member of the AVI stream header. For more information, see <a href="/windows/desktop/DirectShow/dv-data-in-the-avi-file-format">DV Data in the AVI File Format</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>
