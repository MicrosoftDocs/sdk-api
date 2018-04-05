---
UID: NF:icm.GetPS2ColorRenderingIntent
title: GetPS2ColorRenderingIntent function
author: windows-driver-content
description: The GetPS2ColorRenderingIntent function retrieves the PostScript Level 2 color rendering intent from an ICC color profile.
old-location: wcs\getps2colorrenderingintent.htm
old-project: WCS
ms.assetid: 15fdaccc-1a24-4f8f-afed-0f9d141f116f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetPS2ColorRenderingIntent, GetPS2ColorRenderingIntent function [Windows Color System], _color_GetPS2ColorRenderingIntent, icm/GetPS2ColorRenderingIntent, wcs.getps2colorrenderingintent
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
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	GetPS2ColorRenderingIntent
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetPS2ColorRenderingIntent function


## -description


The <b>GetPS2ColorRenderingIntent</b> function retrieves the PostScript Level 2 color <a href="r.htm">rendering intent</a> from an ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param dwIntent

Specifies the desired rendering intent to retrieve. Valid values are:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param pBuffer

Points to a buffer in which the color rendering intent is to be placed. If the <i>pBuffer</i> pointer is set to <b>NULL</b>, the buffer size required is returned in <i>*pcbSize</i>.


### -param pcbPS2ColorRenderingIntent

TBD




#### - pcbSize

Points to a variable containing the buffer size in bytes. On return, this variable contains the number of bytes actually copied.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if the <i>pBuffer</i> parameter is <b>NULL</b> and the size required for the buffer is copied into <i>pcbSize.</i>

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



The rendering intent returned by <b>GetPS2ColorRenderingIntent</b> can be used as the operand for the PostScript Level 2 findcolorrendering operator.

This method does not support WCS profiles.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

