---
UID: NS:vmr9._VMR9ProcAmpControlRange
title: VMR9ProcAmpControlRange (vmr9.h)
description: The VMR9ProcAmpControlRange structure specifies the valid range for an image adjustment property. The range depends on the graphics device driver. This structure is used with the Video Mixing Renderer 9 Filter (VMR-9).
helpviewer_keywords: ["VMR9ProcAmpControlRange","VMR9ProcAmpControlRange structure [DirectShow]","VMR9ProcAmpControlRangeStructure","dshow.vmr9procampcontrolrange","vmr9/VMR9ProcAmpControlRange"]
old-location: dshow\vmr9procampcontrolrange.htm
tech.root: dshow
ms.assetid: 5fa61ed8-4fd6-42fb-8c5b-87d23e239cd1
ms.date: 4/26/2023
ms.keywords: VMR9ProcAmpControlRange, VMR9ProcAmpControlRange structure [DirectShow], VMR9ProcAmpControlRangeStructure, dshow.vmr9procampcontrolrange, vmr9/VMR9ProcAmpControlRange
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
req.typenames: VMR9ProcAmpControlRange
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9ProcAmpControlRange
 - vmr9/_VMR9ProcAmpControlRange
 - VMR9ProcAmpControlRange
 - vmr9/VMR9ProcAmpControlRange
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
 - VMR9ProcAmpControlRange
---

# VMR9ProcAmpControlRange structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9ProcAmpControlRange</code> structure specifies the valid range for an image adjustment property. The range depends on the graphics device driver. This structure is used with the Video Mixing Renderer 9 Filter (VMR-9).

## -struct-fields

### -field dwSize

Size of the structure, in bytes. The value must be <code>sizeof(VMR9ProcAmpControlRange)</code>.

### -field dwProperty

Specifies the image adjustment property to query, as a member of the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9procampcontrolflags">VMR9ProcAmpControlFlags</a> enumeration. The caller should set this field.

### -field MinValue

Specifies the minimum value for the property. The driver sets this field.

### -field MaxValue

Specifies the maximum value for the property. The driver sets this field.

### -field DefaultValue

Specifies the default value for the property. The default value is the value that does not alter the image. The driver sets this field.

### -field StepSize

Specifies the valid increments from <b>MinValue</b> to <b>MaxValue</b>. The driver sets this field.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getprocampcontrolrange">IVMRMixerControl9::GetProcAmpControlRange</a>