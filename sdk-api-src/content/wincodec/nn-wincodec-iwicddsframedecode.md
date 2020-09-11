---
UID: NN:wincodec.IWICDdsFrameDecode
title: IWICDdsFrameDecode (wincodec.h)
description: Provides access to a single frame of DDS image data in its native DXGI_FORMAT form, as well as information about the image data.
helpviewer_keywords: ["IWICDdsFrameDecode","IWICDdsFrameDecode interface [Windows Imaging Component]","IWICDdsFrameDecode interface [Windows Imaging Component]","described","wic.iwicddsframedecode","wincodec/IWICDdsFrameDecode"]
old-location: wic\iwicddsframedecode.htm
tech.root: wic
ms.assetid: 52E76A8D-E7E2-46F5-BBCC-B7C74F1B1122
ms.date: 12/05/2018
ms.keywords: IWICDdsFrameDecode, IWICDdsFrameDecode interface [Windows Imaging Component], IWICDdsFrameDecode interface [Windows Imaging Component],described, wic.iwicddsframedecode, wincodec/IWICDdsFrameDecode
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICDdsFrameDecode
 - wincodec/IWICDdsFrameDecode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDdsFrameDecode
---

# IWICDdsFrameDecode interface


## -description

Provides access to a single frame of DDS image data in its native <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> form, as well as information about the image data.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDdsFrameDecode</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDdsFrameDecode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICDdsFrameDecode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks">CopyBlocks</a>
</td>
<td align="left" width="63%">
Requests pixel data as it is natively stored within the DDS file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-getformatinfo">GetFormatInfo</a>
</td>
<td align="left" width="63%">
Gets information about the format in which the DDS image is stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-getsizeinblocks">GetSizeInBlocks</a>
</td>
<td align="left" width="63%">
Gets the width and height, in blocks, of the DDS image.

</td>
</tr>
</table>

## -remarks

This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> using the DDS codec and QueryInterface for IID_IWICDdsFrameDecode.

