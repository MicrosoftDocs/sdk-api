---
UID: NF:icm.CreateColorTransformA
title: CreateColorTransformA function
author: windows-sdk-content
description: The CreateColorTransform function creates a color transform that applications can use to perform color management.
old-location: wcs\createcolortransform.htm
tech.root: WCS
ms.assetid: 900c97a8-d466-4ecb-86a9-4a92b0e27b44
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateColorTransform, CreateColorTransform function [Windows Color System], CreateColorTransformA, CreateColorTransformW, _color_CreateColorTransform, icm/CreateColorTransform, icm/CreateColorTransformA, icm/CreateColorTransformW, wcs.createcolortransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateColorTransformW (Unicode) and CreateColorTransformA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mscms.dll
api_name:
 - CreateColorTransform
 - CreateColorTransformA
 - CreateColorTransformW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateColorTransformA function


## -description


The <b>CreateColorTransform</b> function creates a color transform that applications can use to perform color management.


## -parameters




### -param pLogColorSpace

Pointer to the input <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a>.


### -param hDestProfile

Handle to the profile of the destination device. The function determines whether the HPROFILE contains International Color Consortium (ICC) or Windows Color System (WCS) profile information.


### -param hTargetProfile

Handle to the profile of the target device. The function determines whether the HPROFILE contains ICC or WCS profile information.


### -param dwFlags

Specifies flags to used control creation of the transform. See Remarks.


## -returns



If this function succeeds, the return value is a handle to the color transform.

If this function fails, the return value is <b>NULL</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the target profile is <b>NULL</b>, the transform goes from the source logical color space to the destination profile. If the target profile is given, the transform goes from the source logical color space to the target profile and then to the destination profile. This allows previewing output meant for the target device on the destination device.

The values in <i>dwFlags</i> are intended as hints only. The color management module must determine the best way to use them.

<b>Windows Vista</b>: Three new flags have been added that can be used with <i>dwFlags</i>:

<table>
<tr>
<td><b>PRESERVEBLACK</b></td>
<td>If this bit is set, the transform engine inserts the appropriate black generation GMMP as the last GMMP in the transform sequence. This flag only works in a pure WCS transform.</td>
</tr>
<tr>
<td><b>SEQUENTIAL_TRANSFORM</b></td>
<td>If this bit is set, each step in the WCS processing pipeline is performed for every pixel in the image and no optimized color transform is built. This flag only works in a pure WCS transform.<b>Restrictions</b>: A transform created with the SEQUENTIAL_TRANSFORM flag set may only be used in the thread on which it was created and only for one color translation call at a time. COM must be initialized prior to creating the sequential transform and must remain initialized for the lifetime of the transform object.

</td>
</tr>
<tr>
<td><b>WCS_ALWAYS</b></td>
<td>If this bit is set, even all-ICC transforms will use the WCS code path.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <b>SEQUENTIAL_TRANSFORM</b> was inadvertently omitted from the icm.h header in the Windows Vista SDK. If you wish to use the <b>SEQUENTIAL_TRANSFORM</b> flag, define it in your application as follows:#define SEQUENTIAL_TRANSFORM 0x80800000</div>
<div> </div>
For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>. All of the flags mentioned there are supported for all types of transforms, except for FAST_TRANSLATE, which only works in a pure ICC-to-ICC transform.

The <b>CreateColorTransform</b> function is used outside of a device context. Colors may shift when transforming from a color profile to the same color profile. This is due to precision errors. Therefore, a color transform should not be performed under these circumstances.

The B2Ax tags are required for any profile that is the target of a transform.

WCS transform support for ICC ColorSpace profiles is limited to RGB colorspace profiles. The following ICC profile types cannot be used in a CITE-processed transform, either a mixed WCS/ICC transform or an all-ICC transform with <b>WCS_ALWAYS</b> set:

<ul>
<li>Non-RGB ColorSpace profiles</li>
<li>NamedColor profiles</li>
<li>n-channel profiles (where n &gt; 8)</li>
<li>DeviceLink profiles</li>
<li>Abstract profiles</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

