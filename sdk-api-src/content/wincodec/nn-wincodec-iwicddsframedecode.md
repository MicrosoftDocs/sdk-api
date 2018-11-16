---
UID: NN:wincodec.IWICDdsFrameDecode
title: IWICDdsFrameDecode
author: windows-sdk-content
description: Provides access to a single frame of DDS image data in its native DXGI_FORMAT form, as well as information about the image data.
old-location: wic\iwicddsframedecode.htm
tech.root: wic
ms.assetid: 52E76A8D-E7E2-46F5-BBCC-B7C74F1B1122
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICDdsFrameDecode, IWICDdsFrameDecode interface [Windows Imaging Component], IWICDdsFrameDecode interface [Windows Imaging Component],described, wic.iwicddsframedecode, wincodec/IWICDdsFrameDecode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDdsFrameDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDdsFrameDecode interface


## -description


Provides access to a single frame of DDS image data in its native <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> form, as well as information about the image data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDdsFrameDecode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICDdsFrameDecode</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D090AA8E-46F2-40C9-A156-12038053E040">CopyBlocks</a>
</td>
<td align="left" width="63%">
Requests pixel data as it is natively stored within the DDS file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D5B9E45-E1EA-4D16-B793-63FEAB2BAF65">GetFormatInfo</a>
</td>
<td align="left" width="63%">
Gets information about the format in which the DDS image is stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34F3A19C-4B68-4E6A-AE08-71DE9A0687BF">GetSizeInBlocks</a>
</td>
<td align="left" width="63%">
Gets the width and height, in blocks, of the DDS image.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the WIC DDS codec. To obtain this interface, create an <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> using the DDS codec and QueryInterface for IID_IWICDdsFrameDecode.



