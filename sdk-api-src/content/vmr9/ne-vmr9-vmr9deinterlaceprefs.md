---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0013_0001
title: VMR9DeinterlacePrefs (vmr9.h)
description: The VMR9DeinterlacePrefs enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 9 (VMR-9) uses if the method set by the application cannot be used.
helpviewer_keywords: ["DeinterlacePref9_BOB","DeinterlacePref9_Mask","DeinterlacePref9_NextBest","DeinterlacePref9_Weave","VMR9DeinterlacePrefs","VMR9DeinterlacePrefs","VMR9DeinterlacePrefs enumeration [DirectShow]","VMR9DeinterlacePrefsEnumeration","dshow.vmr9deinterlaceprefs","vmr9/DeinterlacePref9_BOB","vmr9/DeinterlacePref9_Mask","vmr9/DeinterlacePref9_NextBest","vmr9/DeinterlacePref9_Weave","vmr9/VMR9DeinterlacePrefs"]
old-location: dshow\vmr9deinterlaceprefs.htm
tech.root: dshow
ms.assetid: 1e5f5749-bdf9-4220-9867-ba6899797850
ms.date: 4/26/2023
ms.keywords: DeinterlacePref9_BOB, DeinterlacePref9_Mask, DeinterlacePref9_NextBest, DeinterlacePref9_Weave, VMR9DeinterlacePrefs, VMR9DeinterlacePrefs , VMR9DeinterlacePrefs enumeration [DirectShow], VMR9DeinterlacePrefsEnumeration, dshow.vmr9deinterlaceprefs, vmr9/DeinterlacePref9_BOB, vmr9/DeinterlacePref9_Mask, vmr9/DeinterlacePref9_NextBest, vmr9/DeinterlacePref9_Weave, vmr9/VMR9DeinterlacePrefs
req.header: vmr9.h
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
req.typenames: VMR9DeinterlacePrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0013_0001
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0013_0001
 - VMR9DeinterlacePrefs
 - vmr9/VMR9DeinterlacePrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9DeinterlacePrefs
---

# VMR9DeinterlacePrefs enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9DeinterlacePrefs</code> enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 9 (VMR-9) uses if the method set by the application cannot be used.

## -enum-fields

### -field DeinterlacePref9_NextBest:0x1

Use the next best mode offered by the driver.

### -field DeinterlacePref9_BOB:0x2

Use the bob method.

### -field DeinterlacePref9_Weave:0x4

Use the weave method (that is, no deinterlacing).

### -field DeinterlacePref9_Mask:0x7

Bitwise OR of the previous flags. This value is used internally by the VMR, and is not a valid flag.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrdeinterlacecontrol9">IVMRDeinterlaceControl9 Interface</a>
