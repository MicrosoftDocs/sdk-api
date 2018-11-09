---
UID: NF:icm.CMCreateMultiProfileTransform
title: CMCreateMultiProfileTransform function
author: windows-sdk-content
description: The CMCreateMultiProfileTransform function accepts an array of profiles or a single device link profile and creates a color transform.
old-location: wcs\cmcreatemultiprofiletransform.htm
tech.root: WCS
ms.assetid: 8a40215c-6c37-4346-a669-79b7871f265e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CMCreateMultiProfileTransform, CMCreateMultiProfileTransform function [Windows Color System], _color_CMCreateMultiProfileTransform, icm/CMCreateMultiProfileTransform, wcs.cmcreatemultiprofiletransform
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Icm32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMCreateMultiProfileTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMCreateMultiProfileTransform function


## -description


The <b>CMCreateMultiProfileTransform</b> function accepts an array of profiles or a single <a href="d.htm">device link profile</a> and creates a color transform. This transform is a mapping from the color space specified by the first profile to that of the second profile and so on to the last one.


## -parameters




### -param pahProfiles

TBD


### -param nProfiles

Specifies the number of profiles in the array.


### -param padwIntents

Points to an array of rendering intents. Each rendering intent is represented by one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param nIntents

Specifies the number of intents in the intent array. Can be 1, or the same value as <i>nProfiles</i>.


### -param dwFlags

Specifies flags to used control creation of the transform. For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>.


#### - lpahProfiles

Points to an array of profile handles.


## -returns



If this function succeeds, the return value is a color transform in the range 256 to 65,535. Since only the low <b>WORD</b> of the transform is retained, valid transforms cannot exceed this range.

If this function fails, the return value is an error code having a value less than 256. When the return value is less than 256, signaling an error, the CMM should use <b>SetLastError</b> to set the last error to a valid error value as defined in Winerror.h.




## -remarks



Every CMM is required to export this function.

The array of intents specifies how profiles should be combined. The <i>n</i>th intent is used for combining the <i>n</i>th profile in the array. If only one intent is specified, it is used for the first profile, and all other profiles are combined using Match intent.

The profile handles used to create the color transform can be closed after the call to <b>CMCreateMultiProfileTransform</b> completes.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

