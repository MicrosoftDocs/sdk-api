---
UID: NE:mfobjects._MFVideoFlags
title: "_MFVideoFlags"
author: windows-sdk-content
description: Contains flags that describe a video stream.
old-location: mf\mfvideoflags.htm
tech.root: medfound
ms.assetid: 2530bf1d-05b1-4c16-b00b-117c0dadb301
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 2530bf1d-05b1-4c16-b00b-117c0dadb301, MFVideoFlag_AnalogProtected, MFVideoFlag_BottomUpLinearRep, MFVideoFlag_DigitallyProtected, MFVideoFlag_FieldRepeatCountMask, MFVideoFlag_FieldRepeatCountShift, MFVideoFlag_LowerFieldFirst, MFVideoFlag_PAD_TO_16x9, MFVideoFlag_PAD_TO_4x3, MFVideoFlag_PAD_TO_Mask, MFVideoFlag_PAD_TO_None, MFVideoFlag_PanScanEnabled, MFVideoFlag_ProgressiveContent, MFVideoFlag_ProgressiveSeqReset, MFVideoFlag_SrcContentHint16x9, MFVideoFlag_SrcContentHint235_1, MFVideoFlag_SrcContentHintMask, MFVideoFlag_SrcContentHintNone, MFVideoFlags, MFVideoFlags enumeration [Media Foundation], MFVideoFlags_DXVASurface, MFVideoFlags_ForceQWORD, MFVideoFlags_RenderTargetSurface, _MFVideoFlags, mf.mfvideoflags, mfobjects/MFVideoFlag_AnalogProtected, mfobjects/MFVideoFlag_BottomUpLinearRep, mfobjects/MFVideoFlag_DigitallyProtected, mfobjects/MFVideoFlag_FieldRepeatCountMask, mfobjects/MFVideoFlag_FieldRepeatCountShift, mfobjects/MFVideoFlag_LowerFieldFirst, mfobjects/MFVideoFlag_PAD_TO_16x9, mfobjects/MFVideoFlag_PAD_TO_4x3, mfobjects/MFVideoFlag_PAD_TO_Mask, mfobjects/MFVideoFlag_PAD_TO_None, mfobjects/MFVideoFlag_PanScanEnabled, mfobjects/MFVideoFlag_ProgressiveContent, mfobjects/MFVideoFlag_ProgressiveSeqReset, mfobjects/MFVideoFlag_SrcContentHint16x9, mfobjects/MFVideoFlag_SrcContentHint235_1, mfobjects/MFVideoFlag_SrcContentHintMask, mfobjects/MFVideoFlag_SrcContentHintNone, mfobjects/MFVideoFlags, mfobjects/MFVideoFlags_DXVASurface, mfobjects/MFVideoFlags_ForceQWORD, mfobjects/MFVideoFlags_RenderTargetSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFVideoFlags
product: Windows
targetos: Windows
req.typenames: MFVideoFlags
req.redist: 
---

# _MFVideoFlags enumeration


## -description


Contains flags that describe a video stream.

These flags are used in the <a href="https://msdn.microsoft.com/746fd84f-58f8-42ab-bcf7-8fd18dcd02af">MFVideoInfo</a> structure, which is part of the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.


## -enum-fields




### -field MFVideoFlag_PAD_TO_Mask

Use this value to mask out the next three flags, which describe the effective aspect ratio of the image. This value by itself is not a valid flag.


### -field MFVideoFlag_PAD_TO_None

Do not modify the picture aspect ratio.


### -field MFVideoFlag_PAD_TO_4x3

Display the image in a 4 x 3 area. If this flag is set, the geometrical aperture of the picture should be expanded to a 4 x 3 area by letterboxing or pillarboxing. The geometrical aperture is the portion of the image that is intended to be viewed, without any overscan region.


### -field MFVideoFlag_PAD_TO_16x9

Display the image in a 16 x 9 area. If this flag is set, the geometrical aperture of the picture should be expanded to a 16 x 9 area by letterboxing or pillarboxing.


### -field MFVideoFlag_SrcContentHintMask

Use this value to mask out the next three flags, which describe the source content. This value by itself is not a valid flag.


### -field MFVideoFlag_SrcContentHintNone

There is no additional information about the source content .


### -field MFVideoFlag_SrcContentHint16x9

The source is a 16 x 9 image encoded within a 4 x 3 area.


### -field MFVideoFlag_SrcContentHint235_1

The source is a 2.35:1 image encoded within a 16 x 9 or 4 x 3 area.


### -field MFVideoFlag_AnalogProtected

Analog copy protection should be applied.


### -field MFVideoFlag_DigitallyProtected

Digital copy protection should be applied.


### -field MFVideoFlag_ProgressiveContent

The video source is progressive content encoded as interlaced video, possibly using 3:2 pulldown. This flag is obsolete. See Remarks.


### -field MFVideoFlag_FieldRepeatCountMask

Used to extract the field repeat count. This flag is obsolete. See Remarks.


### -field MFVideoFlag_FieldRepeatCountShift

Used to extract the field repeat count. This flag is obsolete. See Remarks.


### -field MFVideoFlag_ProgressiveSeqReset

The progressive sequence was disrupted and the sequence is interlaced at the break. This flag is obsolete. See Remarks.


### -field MFVideoFlag_PanScanEnabled

Apply the pan and scan rectangle on the output.


### -field MFVideoFlag_LowerFieldFirst

The sample contains the lower field. This flag applies only if the interlace mode is single fields (MFVideoInterlace_FieldSingleUpperFirst or MFVideoInterlace_FieldSingleLowerFirst). This flag is obsolete. See Remarks.


### -field MFVideoFlag_BottomUpLinearRep

The image is represented bottom-up in memory. This flag should be used only with RGB formats.


### -field MFVideoFlags_DXVASurface

Reserved. Do not use.


### -field MFVideoFlags_RenderTargetSurface

Reserved. Do not use.


### -field MFVideoFlags_ForceQWORD

Reserved. This member forces the enumeration type to compile as a <b>QWORD</b> value.


## -remarks



Developers are encouraged to use media type attributes instead of using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure. The following table lists the attributes that correspond to the flags defined in this enumeration.

<table>
<tr>
<th>Flags</th>
<th>Media Type Attribute</th>
</tr>
<tr>
<td>
MFVideoFlag_PAD_TO_None

MFVideoFlag_PAD_TO_4x3

MFVideoFlag_PAD_TO_16x9

</td>
<td>
<a href="https://msdn.microsoft.com/d7fec5fb-a1fe-4cc9-aa27-a3af0456ea8d">MF_MT_PAD_CONTROL_FLAGS</a>
</td>
</tr>
<tr>
<td>
MFVideoFlag_SrcContentHint16x9

MFVideoFlag_SrcContentHint16x9

MFVideoFlag_SrcContentHint235_1

</td>
<td>
<a href="https://msdn.microsoft.com/6b32e257-c523-4859-8c8f-661c33810624">MF_MT_SOURCE_CONTENT_HINT</a>
</td>
</tr>
<tr>
<td>
MFVideoFlag_AnalogProtected

MFVideoFlag_DigitallyProtected

</td>
<td>
<a href="https://msdn.microsoft.com/fb12ba38-a4f4-44fe-bf31-e731c56bb145">MF_MT_DRM_FLAGS</a>
</td>
</tr>
<tr>
<td>MFVideoFlag_PanScanEnabled</td>
<td>
<a href="https://msdn.microsoft.com/9e8746c6-13a4-4cf7-9748-82223d9529fa">MF_MT_PAN_SCAN_ENABLED</a>
</td>
</tr>
<tr>
<td>MFVideoFlag_BottomUpLinearRep</td>
<td>Use the <a href="https://msdn.microsoft.com/71fda231-3497-49db-b82e-2fd79f6ade66">MF_MT_DEFAULT_STRIDE</a> attribute to specify a negative stride.</td>
</tr>
</table>
 

The following flags were defined to describe per-sample interlacing information, but are obsolete:

<ul>
<li>MFVideoFlag_ProgressiveContent
          </li>
<li>MFVideoFlag_FieldRepeatCountMask
          </li>
<li>MFVideoFlag_FieldRepeatCountShift
          </li>
<li>MFVideoFlag_ProgressiveSeqReset
          </li>
<li>MFVideoFlag_LowerFieldFirst
            
          </li>
</ul>
Instead, components should use sample attributes to describe per-sample interlacing information, as described in the topic <a href="https://msdn.microsoft.com/2911ae57-1703-4a9d-bd33-94af1e0f8804">Video Interlacing</a>.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

