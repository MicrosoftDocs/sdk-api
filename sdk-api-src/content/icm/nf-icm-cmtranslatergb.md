---
UID: NF:icm.CMTranslateRGB
title: CMTranslateRGB function
author: windows-sdk-content
description: The CMTranslateRGB function translates an application-supplied RGBQuad into the device color space.
old-location: wcs\cmtranslatergb.htm
tech.root: WCS
ms.assetid: b6ae9190-007e-43f0-b5d9-7eda372e2c02
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CMS_BACKWARD, CMS_FORWARD, CMTranslateRGB, CMTranslateRGB function [Windows Color System], _color_CMTranslateRGB, icm/CMTranslateRGB, wcs.cmtranslatergb
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
 - CMTranslateRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMTranslateRGB function


## -description


The <b>CMTranslateRGB</b> function translates an application-supplied RGBQuad into the device <a href="c.htm">color space</a>.


## -parameters




### -param hcmTransform

Specifies the transform to be used.


### -param ColorRef

The RGBQuad to translate.


### -param lpColorRef

Points to a buffer in which to place the translation.


### -param dwFlags

Specifies how the transform should be used to make the translation. This parameter can take one of the following meanings.<div> </div>


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



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. The CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

