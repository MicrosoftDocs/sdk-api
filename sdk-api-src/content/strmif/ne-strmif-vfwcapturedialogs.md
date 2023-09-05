---
UID: NE:strmif.VfwCaptureDialogs
title: VfwCaptureDialogs (strmif.h)
description: Specifies a dialog box that might exist in a Video for Windows capture driver.
helpviewer_keywords: ["VfwCaptureDialog_Display","VfwCaptureDialog_Format","VfwCaptureDialog_Source","VfwCaptureDialogs","VfwCaptureDialogs enumeration [DirectShow]","VfwCaptureDialogsEnumeration","dshow.vfwcapturedialogs","strmif/VfwCaptureDialog_Display","strmif/VfwCaptureDialog_Format","strmif/VfwCaptureDialog_Source","strmif/VfwCaptureDialogs"]
old-location: dshow\vfwcapturedialogs.htm
tech.root: dshow
ms.assetid: 0465d887-6452-4a67-9f52-a459620d12d2
ms.date: 4/26/2023
ms.keywords: VfwCaptureDialog_Display, VfwCaptureDialog_Format, VfwCaptureDialog_Source, VfwCaptureDialogs, VfwCaptureDialogs enumeration [DirectShow], VfwCaptureDialogsEnumeration, dshow.vfwcapturedialogs, strmif/VfwCaptureDialog_Display, strmif/VfwCaptureDialog_Format, strmif/VfwCaptureDialog_Source, strmif/VfwCaptureDialogs
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
req.typenames: VfwCaptureDialogs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VfwCaptureDialogs
 - strmif/VfwCaptureDialogs
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
 - VfwCaptureDialogs
---

# VfwCaptureDialogs enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies a dialog box that might exist in a Video for Windows capture driver.

## -enum-fields

### -field VfwCaptureDialog_Source:0x1

Video source dialog box.

### -field VfwCaptureDialog_Format:0x2

Video format dialog box.

### -field VfwCaptureDialog_Display:0x4

Video display dialog box.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcapturedialogs">IAMVfwCaptureDialogs Interface</a>
