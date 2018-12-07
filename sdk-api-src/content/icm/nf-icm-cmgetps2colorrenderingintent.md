---
UID: NF:icm.CMGetPS2ColorRenderingIntent
title: CMGetPS2ColorRenderingIntent function
author: windows-sdk-content
description: The CMGetPS2ColorRenderingIntent function retrieves the PostScript Level 2 color rendering intent from a profile.
old-location: wcs\cmgetps2colorrenderingintent.htm
tech.root: WCS
ms.assetid: 2cb056d1-a3d5-4492-80ed-07c34f80c8db
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMGetPS2ColorRenderingIntent, CMGetPS2ColorRenderingIntent function [Windows Color System], _color_CMGetPS2ColorRenderingIntent, icm/CMGetPS2ColorRenderingIntent, wcs.cmgetps2colorrenderingintent
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
 - CMGetPS2ColorRenderingIntent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMGetPS2ColorRenderingIntent
: 
---

# CMGetPS2ColorRenderingIntent function


## -description


The <b>CMGetPS2ColorRenderingIntent</b> function retrieves the PostScript Level 2 color <a href="r.htm">rendering intent</a> from a profile.


## -parameters




### -param hProfile

Specifies the profile to use.


### -param dwIntent

Specifies the desired rendering intent to retrieve. Can be one of the following values:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param lpBuffer

Points to a buffer in which the color rendering intent is to be placed. If the pointer is <b>NULL</b>, the function returns the size required for this buffer in <i>*lpcbSize</i>.


### -param lpcbSize

Points to a variable specifying the size of the buffer. On return, the variable contains has the number of bytes actually copied to the buffer.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if it is called with <i>lpBuffer</i> set to <b>NULL</b> and the size of the required buffer is copied into <i>lpcbSize</i>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is optional for all CMMs.

If a CMM does not support this function, Windows uses the default CMM to get the color rendering intent.

If the tag is not present in the profile indicated by <i>hProfile</i>, the CMM creates it. The resulting rendering intent can be used as the operand for the PostScript Level 2 <b>findcolorrendering</b> operator.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

