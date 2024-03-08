---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0005_0002
title: VMR9ProcAmpControlFlags (vmr9.h)
description: The VMR9ProcAmpControlFlags enumeration type specifies image adjustment properties, for use with the Video Mixing Render Filter 9 (VMR-9).
helpviewer_keywords: ["ProcAmpControl9_Brightness","ProcAmpControl9_Contrast","ProcAmpControl9_Hue","ProcAmpControl9_Mask","ProcAmpControl9_Saturation","VMR9ProcAmpControlFlags","VMR9ProcAmpControlFlags","VMR9ProcAmpControlFlags enumeration [DirectShow]","dshow.vmr9procampcontrolflags","vmr9/ProcAmpControl9_Brightness","vmr9/ProcAmpControl9_Contrast","vmr9/ProcAmpControl9_Hue","vmr9/ProcAmpControl9_Mask","vmr9/ProcAmpControl9_Saturation","vmr9/VMR9ProcAmpControlFlags"]
old-location: dshow\vmr9procampcontrolflags.htm
tech.root: dshow
ms.assetid: 5dfba718-4c89-46e7-89b6-e4b133b0ce04
ms.date: 4/26/2023
ms.keywords: ProcAmpControl9_Brightness, ProcAmpControl9_Contrast, ProcAmpControl9_Hue, ProcAmpControl9_Mask, ProcAmpControl9_Saturation, VMR9ProcAmpControlFlags, VMR9ProcAmpControlFlags , VMR9ProcAmpControlFlags enumeration [DirectShow], dshow.vmr9procampcontrolflags, vmr9/ProcAmpControl9_Brightness, vmr9/ProcAmpControl9_Contrast, vmr9/ProcAmpControl9_Hue, vmr9/ProcAmpControl9_Mask, vmr9/ProcAmpControl9_Saturation, vmr9/VMR9ProcAmpControlFlags
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
req.typenames: VMR9ProcAmpControlFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0005_0002
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0005_0002
 - VMR9ProcAmpControlFlags
 - vmr9/VMR9ProcAmpControlFlags
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
 - VMR9ProcAmpControlFlags
---

# VMR9ProcAmpControlFlags enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9ProcAmpControlFlags</code> enumeration type specifies image adjustment properties, for use with the Video Mixing Render Filter 9 (VMR-9).

## -enum-fields

### -field ProcAmpControl9_Brightness:0x1

Brightness adjustment.

### -field ProcAmpControl9_Contrast:0x2

Contrast adjustment.

### -field ProcAmpControl9_Hue:0x4

Hue adjustment.

### -field ProcAmpControl9_Saturation:0x8

Saturation adjustment.

### -field ProcAmpControl9_Mask:0xf

Bitwise <b>OR</b> of all the previous flags. This value is used internally by the VMR-9, and is not a valid flag.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9procampcontrol">VMR9ProcAmpControl Structure</a>



<a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9procampcontrolrange">VMR9ProcAmpControlRange Structure</a>
