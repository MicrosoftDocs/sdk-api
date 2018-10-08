---
UID: NF:icm.CMGetPS2ColorRenderingDictionary
title: CMGetPS2ColorRenderingDictionary function
author: windows-sdk-content
description: The CMGetPS2ColorRenderingDictionary function retrieves the PostScript Level 2 color rendering dictionary for a given rendering intent from a given profile.
old-location: wcs\cmgetps2colorrenderingdictionary.htm
tech.root: WCS
ms.assetid: bf67fd0a-d32d-41e6-8868-ceb7bc8cd2f4
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: CMGetPS2ColorRenderingDictionary, CMGetPS2ColorRenderingDictionary function [Windows Color System], _color_CMGetPS2ColorRenderingDictionary, icm/CMGetPS2ColorRenderingDictionary, wcs.cmgetps2colorrenderingdictionary
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
 - CMGetPS2ColorRenderingDictionary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMGetPS2ColorRenderingDictionary function


## -description


The <b>CMGetPS2ColorRenderingDictionary</b> function retrieves the PostScript Level 2 color rendering dictionary for a given <a href="r.htm">rendering intent</a> from a given profile.


## -parameters




### -param hProfile

Specifies the profile to use.


### -param dwIntent

Specifies the rendering intent. Can be one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param lpBuffer

Pointer to a buffer in which the color rendering dictionary is to be placed. If the pointer is <b>NULL</b>, the function returns the size required for this buffer in the memory location pointed to by <i>lpcbSize</i>.


### -param lpcbSize

Pointer to a variable specifying the size of the buffer. On return, the variable contains the number of bytes actually copied to the buffer.


### -param lpbBinary

Points to a Boolean variable. If its value is <b>TRUE</b>, data returned could be binary, or if <b>FALSE</b>, the data should be ASCII85 encoded. On return, the value pointed to by <i>lpbBinary</i> indicates whether the data returned actually is binary or ASCII85.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if it is called with <i>lpBuffer</i> set to <b>NULL</b> and the size of the required buffer is copied into <i>lpcbSize</i>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is optional for all CMMs.

If a CMM does not support this function, Windows uses the default CMM to create the color rendering dictionary.

If the color rendering dictionary tag is not present in the profile indicated by <i>hProfile</i>, the CMM creates the color rendering dictionary from the profile contents. The resulting color rendering dictionary can be used as the operand for the PostScript Level 2 <b>setcolorrendering</b> operator.

This function fails if the profile indicated by <i>hProfile</i> does not have LUT tags associated with it. For more information on LUT tags, see the ICC Profile Format Specification available at www.color.org.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

