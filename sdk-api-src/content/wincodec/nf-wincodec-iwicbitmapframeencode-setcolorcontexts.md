---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWICBitmapFrameEncode::SetColorContexts


## -description


Sets a given number <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> profiles to the frame.


## -parameters




### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> profiles to set.


### -param ppIColorContext [in]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

A pointer to an <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> pointer containing the color contexts profiles to set to the frame.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<ul>
<li><b>BMP</b>Setting color contexts is unsupported. This function will return <b>WINCODEC_ERR_UNSUPPORTEDOPERATION</b>.

</li>
<li><b>PNG</b>Setting at most one color context is supported, and additional color contexts will be ignored. This context must be a <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a>, and is used to encode the iCCP, gAMA, and cHRM chunks in the PNG file.

</li>
<li><b>JPEG, TIFF, JPEG-XR</b>Setting up to one <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a> and one  <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextExifColorSpace</a> is supported. Users must not provide more than one of each type of color context, as all but the last context of each type will be ignored. In JPEG, the <b>WICColorContextProfile</b> is encoded to JPEG APP2 ICC metadata block.

In TIFF and JPEG-XR, the  <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextProfile</a> is encoded to the IFD ICC profile metadata block (IFD tag 0x8773). In all three formats, the <a href="_wic_codec_wiccolorcontexttype.htm">WICColorContextExifColorSpace</a> is encoded to EXIF colorspace metadata block (EXIF tag 0xA001).


</li>
</ul>


