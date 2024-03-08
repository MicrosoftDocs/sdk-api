---
UID: NE:strmif.VMRDeinterlacePrefs
title: VMRDeinterlacePrefs (strmif.h)
description: The VMRDeinterlacePrefs enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 7 (VMR-7) uses if the method set by the application cannot be used.
helpviewer_keywords: ["DeinterlacePref_BOB","DeinterlacePref_Mask","DeinterlacePref_NextBest","DeinterlacePref_Weave","VMRDeinterlacePrefs","VMRDeinterlacePrefs enumeration [DirectShow]","VMRDeinterlacePrefsEnumeration","dshow.vmrdeinterlaceprefs","strmif/DeinterlacePref_BOB","strmif/DeinterlacePref_Mask","strmif/DeinterlacePref_NextBest","strmif/DeinterlacePref_Weave","strmif/VMRDeinterlacePrefs"]
old-location: dshow\vmrdeinterlaceprefs.htm
tech.root: dshow
ms.assetid: 3f88abac-fc57-4f31-9a4c-cf0f7317d6f8
ms.date: 4/26/2023
ms.keywords: DeinterlacePref_BOB, DeinterlacePref_Mask, DeinterlacePref_NextBest, DeinterlacePref_Weave, VMRDeinterlacePrefs, VMRDeinterlacePrefs enumeration [DirectShow], VMRDeinterlacePrefsEnumeration, dshow.vmrdeinterlaceprefs, strmif/DeinterlacePref_BOB, strmif/DeinterlacePref_Mask, strmif/DeinterlacePref_NextBest, strmif/DeinterlacePref_Weave, strmif/VMRDeinterlacePrefs
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
req.typenames: VMRDeinterlacePrefs
req.redist: 
req.product: Windows XP with SP1
ms.custom: 19H1
f1_keywords:
 - VMRDeinterlacePrefs
 - strmif/VMRDeinterlacePrefs
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
 - VMRDeinterlacePrefs
---

# VMRDeinterlacePrefs enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VMRDeinterlacePrefs</b> enumeration type describes the deinterlacing method that the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7) uses if the method set by the application cannot be used.

## -enum-fields

### -field DeinterlacePref_NextBest:0x1

Use the next best mode offered by the driver.

### -field DeinterlacePref_BOB:0x2

Use the bob method.

### -field DeinterlacePref_Weave:0x4

Use the weave method (that is, no deinterlacing).

### -field DeinterlacePref_Mask:0x7

Bitwise <b>OR</b> of the previous flags. This value is not a valid flag.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>
