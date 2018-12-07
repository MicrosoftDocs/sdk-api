---
UID: NF:icm.GetPS2ColorSpaceArray
title: GetPS2ColorSpaceArray function
author: windows-sdk-content
description: The GetPS2ColorSpaceArray function retrieves the PostScript Level 2 color space array from an ICC color profile.
old-location: wcs\getps2colorspacearray.htm
tech.root: WCS
ms.assetid: d7e0de11-d5fe-4d3f-bdd0-2c6f7c61a0a9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPS2ColorSpaceArray, GetPS2ColorSpaceArray function [Windows Color System], _color_GetPS2ColorSpaceArray, icm/GetPS2ColorSpaceArray, wcs.getps2colorspacearray
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - GetPS2ColorSpaceArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetPS2ColorSpaceArray
: 
---

# GetPS2ColorSpaceArray function


## -description


The <b>GetPS2ColorSpaceArray</b> function retrieves the PostScript Level 2 <a href="c.htm">color space</a> array from an ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC profile from which to retrieve the PostScript Level 2 color space array.


### -param dwIntent

Specifies the desired rendering intent for the color space array. This field may take one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param dwCSAType

Specifies the type of color space array. See <a href="https://msdn.microsoft.com/dc312db2-3bc5-461f-819c-37ff14cff896">Color Space Type Identifiers</a>.


### -param pPS2ColorSpaceArray

Pointer to a buffer in which the color space array is to be placed. If the <i>pBuffer</i> pointer is set to <b>NULL</b>, the function returns the required size of the buffer in the memory location pointed to by <i>pcbSize</i>.


### -param pcbPS2ColorSpaceArray

Pointer to a variable containing the size of the buffer in bytes. On return, it contains the number of bytes copied into the buffer.


### -param pbBinary

Pointer to a Boolean variable. If set to <b>TRUE</b>, the data copied could be binary. If set to <b>FALSE</b>, data should be encoded as ASCII85. On return, the memory location pointed to by <i>pbBinary</i> indicates whether the data returned actually is binary (<b>TRUE</b>) or ASCII85 (<b>FALSE</b>).


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if the <i>pBuffer</i> parameter is <b>NULL</b> and the size required for the buffer is copied into <i>pcbSize.</i>

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the color space array is not available in the profile, the <b>GetPS2ColorSpaceArray</b> function builds a PostScript Level 2 color space array using the profile contents. This array can then be used as the operand for the PostScript Level2 setcolorspace operator.

This method does not support WCS profiles.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

