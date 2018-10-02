---
UID: NF:icm.CMTranslateRGBs
title: CMTranslateRGBs function
author: windows-sdk-content
description: CMTranslateRGBs is no longer available for use as of Windows Vista.
old-location: wcs\cmtranslatergbs.htm
tech.root: WCS
ms.assetid: a9dc34ed-b12d-460e-ba74-51ed681d8484
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CMS_BACKWARD, CMS_FORWARD, CMTranslateRGBs, CMTranslateRGBs function [Windows Color System], _color_CMTranslateRGBs, icm/CMTranslateRGBs, wcs.cmtranslatergbs
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
 - CMTranslateRGBs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMTranslateRGBs function


## -description


<p class="CCE_Message">[<b>CMTranslateRGBs</b> is no longer available for use as of Windows Vista.]

The <b>CMTranslateRGBs</b> function translates a bitmap from one <a href="c.htm">color space</a> to another using a color transform.


## -parameters




### -param hcmTransform

Specifies the color transform to use.


### -param lpSrcBits

Points to the bitmap to translate.


### -param bmInput

Specifies the input bitmap format.


### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.


### -param dwHeight

Specifies the number of scan lines in the input bitmap.


### -param dwStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If <i>dwStride</i> is set to zero, the CMM should assume that scan lines are padded so as to be <b>DWORD</b>-aligned.


### -param lpDestBits

Points to a destination buffer in which to place the translated bitmap.


### -param bmOutput

Specifies the output bitmap format.


### -param dwTranslateDirection

Specifies the direction of the transform being used for the translation. This parameter must take one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMS_FORWARD"></a><a id="cms_forward"></a><dl>
<dt><b>CMS_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
Use forward transform

</td>
</tr>
<tr>
<td width="40%"><a id="CMS_BACKWARD"></a><a id="cms_backward"></a><dl>
<dt><b>CMS_BACKWARD</b></dt>
</dl>
</td>
<td width="60%">
Use reverse transform

</td>
</tr>
</table>
 


## -returns



Beginning with Windows Vista, the default CMM (Icm32.dll) will return <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will report ERROR_NOT_SUPPORTED.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. If the function is not successful, the CMM should call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the last error to a valid error value defined in Winerror.h.






## -remarks



Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>Every CMM is required to export this function.

When writing into the destination buffer, the CMM should make sure that scan lines are padded to be <b>DWORD</b>-aligned.

If the input and output formats are not compatible with the color transform, this function fails.

If both input and output bitmap formats are 3-channel, 4 bytes-per-pixel as in the case of BM_xRGBQUADS, the 4th byte should be preserved and copied to the output buffer.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.






## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

