---
UID: NF:icm.GetPS2ColorRenderingDictionary
title: GetPS2ColorRenderingDictionary function
author: windows-driver-content
description: The GetPS2ColorRenderingDictionary function retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.
old-location: wcs\getps2colorrenderingdictionary.htm
old-project: WCS
ms.assetid: 0dc10487-7b60-4f5d-a5b7-0dd8a6d1c0c5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetPS2ColorRenderingDictionary, GetPS2ColorRenderingDictionary function [Windows Color System], _color_GetPS2ColorRenderingDictionary, icm/GetPS2ColorRenderingDictionary, wcs.getps2colorrenderingdictionary
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
-	GetPS2ColorRenderingDictionary
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetPS2ColorRenderingDictionary function


## -description


The <b>GetPS2ColorRenderingDictionary</b> function retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.


## -parameters




### -param hProfile

Specifies a handle to the ICC color profile in question.


### -param dwIntent

Specifies the desired rendering intent for the color rendering dictionary. Valid values are:

INTENT_PERCEPTUAL<div> </div>INTENT_SATURATION<div> </div>INTENT_RELATIVE_COLORIMETRIC<div> </div>INTENT_ABSOLUTE_COLORIMETRIC

For more information, see <a href="https://msdn.microsoft.com/c980f3ea-daff-491a-a10a-03ba446d383e">Rendering Intents</a>.


### -param pPS2ColorRenderingDictionary

TBD


### -param pcbPS2ColorRenderingDictionary

TBD


### -param pbBinary

Pointer to a Boolean variable. If <b>TRUE</b>, the color rendering dictionary could be copied in binary form. If <b>FALSE</b>, the dictionary will be encoded in ASCII85 form. On return, this Boolean variable indicates whether the dictionary was actually binary (<b>TRUE</b>) or ASCII85 (<b>FALSE</b>).


#### - pBuffer

Pointer to a buffer in which the color rendering dictionary is to be placed. If the <i>pBuffer</i> pointer is set to <b>NULL</b>, the required buffer size is returned in <i>*pcbSize</i>.


#### - pcbSize

Pointer to a variable containing the size of the buffer in bytes. On return, the variable contains the number of bytes actually copied.


## -returns



If this function succeeds, the return value is <b>TRUE</b>. It also returns <b>TRUE</b> if the <i>pBuffer</i> parameter is <b>NULL</b> and the size required for the buffer is copied into <i>pcbSize.</i>

If this function fails, the return value is <b>FALSE</b>.




## -remarks



If the dictionary is not available in the profile, the <b>GetPS2ColorRenderingDictionary</b> function builds one using the profile contents. This dictionary can then be used as the operand for the PostScript Level 2 <b>setcolorrendering</b> operator.

This method does not support WCS profiles.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

