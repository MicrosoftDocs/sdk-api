---
UID: NF:icm.CMGetPS2ColorSpaceArray
title: CMGetPS2ColorSpaceArray function
author: windows-sdk-content
description: The CMGetPS2ColorSpaceArray function retrieves the PostScript Level 2 color space array from a profile.
old-location: wcs\cmgetps2colorspacearray.htm
tech.root: WCS
ms.assetid: 2d7178e0-1535-48ce-8dbe-abd0d95cc294
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CMGetPS2ColorSpaceArray, CMGetPS2ColorSpaceArray function [Windows Color System], _color_CMGetPS2ColorSpaceArray, icm/CMGetPS2ColorSpaceArray, wcs.cmgetps2colorspacearray
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
api_name:
 - CMGetPS2ColorSpaceArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMGetPS2ColorSpaceArray function


## -description


The <b>CMGetPS2ColorSpaceArray</b> function retrieves the PostScript Level 2 color space array from a profile.


## -parameters




### -param hProfile

Specifies the profile to use.


### -param dwIntent

Specifies the desired rendering intent for the color space array. Can be one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param dwCSAType

Specifies the type of color space array. See <a href="https://msdn.microsoft.com/dc312db2-3bc5-461f-819c-37ff14cff896">Color Space Type Identifiers</a>.


### -param lpBuffer

Pointer to a buffer in which the color space array is to be placed. If the pointer is <b>NULL</b>, the function returns the size required for this buffer in the memory location pointed to by <i>lpcbSize</i>.


### -param lpcbSize

Pointer to a variable specifying the size of the buffer. On return, the variable contains has the number of bytes actually copied to the buffer.


### -param lpbBinary

Pointer to a Boolean variable. If its value is <b>TRUE</b>, data returned could be binary, or if <b>FALSE</b>, the data should be ASCII85 encoded. On return, the value of in the memory location pointed to by <i>lpbBinary</i> indicates whether the data returned actually is binary or ASCII85.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if it is called with <i>lpBuffer</i> set to <b>NULL</b> and the size of the required buffer is copied into <i>lpcbSize</i>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is optional for all CMMs.

If a CMM does not support this function, Windows uses the default CMM to create the color space array.

If the color space array tag is not present in the profile, the CMM should create the color space array from the profile contents. The resulting color space array can be used as the operand for the PostScript Level 2 <b>setcolorspace</b> operator.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

