---
UID: NE:strmif.VMRMode
title: VMRMode (strmif.h)
description: The VMRMode enumeration type is used in calls to the IVMRFilterConfig::GetRenderingMode and IVMRFilterConfig::SetRenderingMode methods to retrieve or specify the Video Mixing Renderer Filter 7 (VMR-7) rendering mode.
helpviewer_keywords: ["VMRMode","VMRMode enumeration [DirectShow]","VMRModeEnumeration","VMRMode_Mask","VMRMode_Renderless","VMRMode_Windowed","VMRMode_Windowless","dshow.vmrmode","strmif/VMRMode","strmif/VMRMode_Mask","strmif/VMRMode_Renderless","strmif/VMRMode_Windowed","strmif/VMRMode_Windowless"]
old-location: dshow\vmrmode.htm
tech.root: dshow
ms.assetid: cc924b1a-561f-4d62-8cc8-03ba5e5e8d5b
ms.date: 4/26/2023
ms.keywords: VMRMode, VMRMode enumeration [DirectShow], VMRModeEnumeration, VMRMode_Mask, VMRMode_Renderless, VMRMode_Windowed, VMRMode_Windowless, dshow.vmrmode, strmif/VMRMode, strmif/VMRMode_Mask, strmif/VMRMode_Renderless, strmif/VMRMode_Windowed, strmif/VMRMode_Windowless
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VMRMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VMRMode
 - strmif/VMRMode
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
 - VMRMode
---

# VMRMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VMRMode</b> enumeration type is used in calls to the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingmode">IVMRFilterConfig::GetRenderingMode</a> and <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingmode">IVMRFilterConfig::SetRenderingMode</a> methods to retrieve or specify the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7) rendering mode.

## -enum-fields

### -field VMRMode_Windowed:0x1

Windowed mode.

### -field VMRMode_Windowless:0x2

Windowless mode.

### -field VMRMode_Renderless:0x4

Renderless mode.

### -field VMRMode_Mask:0x7

Bitwise <b>OR</b> of all above flags; this is not a valid value to pass to <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingmode">SetRenderingMode</a>.

## -remarks

These modes are mutually exclusive. The <b>VMRMode_Renderless</b> flag means that the application is providing its own allocator-presenter, which is responsible for all drawing to the screen. The <b>VMRMode_Windowed</b> flag is the default mode of the VMR-7. See <a href="/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a> for more information on the rendering modes.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
