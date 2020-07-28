---
UID: NS:vmr9._VMR9ProcAmpControl
title: VMR9ProcAmpControl (vmr9.h)
description: The VMR9ProcAmpControl structure specifies the image adjustments to be performed on a video stream. This structure is used with the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["VMR9ProcAmpControl","VMR9ProcAmpControl structure [DirectShow]","VMR9ProcAmpControlStructure","dshow.vmr9procampcontrol","vmr9/VMR9ProcAmpControl"]
old-location: dshow\vmr9procampcontrol.htm
tech.root: dshow
ms.assetid: c4395344-e659-4e5a-aba0-ee27e65fe2cc
ms.date: 12/05/2018
ms.keywords: VMR9ProcAmpControl, VMR9ProcAmpControl structure [DirectShow], VMR9ProcAmpControlStructure, dshow.vmr9procampcontrol, vmr9/VMR9ProcAmpControl
f1_keywords:
- vmr9/VMR9ProcAmpControl
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vmr9.h
api_name:
- VMR9ProcAmpControl
targetos: Windows
req.typenames: VMR9ProcAmpControl
req.redist: 
ms.custom: 19H1
---

# VMR9ProcAmpControl structure


## -description



The <code>VMR9ProcAmpControl</code> structure specifies the image adjustments to be performed on a video stream. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9).




## -struct-fields




### -field dwSize

Size of the structure, in bytes. The value must be <code>sizeof(VMR9ProcAmpControl)</code>.


### -field dwFlags

Bitwise combination of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9procampcontrolflags">VMR9ProcAmpControlFlags</a> enumeration, indicating which properties the driver supports.


### -field Brightness

Specifies the image brightness. Brightness, also called black-level setup, specifies the viewing black level. Functionally, it adds or subtracts the same number of quantizing steps (bits) from all the luminance words in a picture.


### -field Contrast

Specifies the image contrast. Contrast alters the relative light-to-dark values in a picture. Functionally it maps the range of input values to a smaller or larger range of output values.


### -field Hue

Specifies the image hue. Perceptually, hue corresponds approximately to "color." Functionally, hue is a phase relationship of the chrominance components. It is specified in degrees, with a nominal valid range from –180 to 180 degrees and a default value of 0.


### -field Saturation

Specifies the image saturation. Saturation alters the color intensity of the image. Functionally it is similar to contrast, but operates on the chroma components of the image.


## -remarks



The valid range of values for each property depends on the graphics device driver. Call the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-getprocampcontrolrange">IVMRMixerControl9::GetProcAmpControlRange</a> method to get the range for each property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

