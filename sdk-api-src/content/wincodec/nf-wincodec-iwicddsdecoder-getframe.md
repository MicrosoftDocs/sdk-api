---
UID: NF:wincodec.IWICDdsDecoder.GetFrame
title: IWICDdsDecoder::GetFrame
author: windows-sdk-content
description: Retrieves the specified frame of the DDS image.
old-location: wic\iwicddsdecoder_getframe.htm
tech.root: wic
ms.assetid: 8842FD14-575B-4A81-9598-83A5A67415B7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFrame, GetFrame method [Windows Imaging Component], GetFrame method [Windows Imaging Component],IWICDdsDecoder interface, IWICDdsDecoder interface [Windows Imaging Component],GetFrame method, IWICDdsDecoder.GetFrame, IWICDdsDecoder::GetFrame, wic.iwicddsdecoder_getframe, wincodec/IWICDdsDecoder::GetFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWICDdsDecoder.GetFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDdsDecoder::GetFrame


## -description


Retrieves the specified frame of the DDS image.


## -parameters




### -param arrayIndex [in]

Type: <b>UINT</b>

The requested index within the texture array.


### -param mipLevel [in]

Type: <b>UINT</b>

The requested mip level.


### -param sliceIndex [in]

Type: <b>UINT</b>

The requested slice within the 3D texture.



### -param ppIBitmapFrame [out]

Type: <b><a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>**</b>

A pointer to a  <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> object.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A DDS file can contain multiple images that are organized into a three level hierarchy. First, DDS file may contain multiple textures in a texture array. Second, each texture can have multiple mip levels. Finally, the texture may be a 3D (volume) texture and have multiple slices, each of which is a 2D texture. See the <a href="https://msdn.microsoft.com/b0f3a1af-e816-4d64-93d9-51e510423869">DDS documentation</a> for more information.

WIC maps this three level hierarchy into a linear array of <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a>, accessible via <a href="https://msdn.microsoft.com/5e8c1cfd-50f3-431c-aedb-6e57d1368695">IWICBitmapDecoder::GetFrame</a>. However, determining which frame corresponds to a triad of <i>arrayIndex</i>, <i>mipLevel</i>, and <i>sliceIndex</i> value is not trivial because each mip level of a 3D texture has a different depth (number of slices). This method provides additional convenience over <b>IWICBitmapDecoder::GetFrame</b> for DDS images by calculating the correct frame given the three indices.





## -see-also




<a href="https://msdn.microsoft.com/76741d1e-3e1b-4018-b092-b668ecfd43c9">CreateBitmap</a>



<a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>



<a href="https://msdn.microsoft.com/632D1E7B-9C1D-48FB-95B5-1A295FE99577">IWICDdsDecoder</a>



<a href="https://msdn.microsoft.com/C5F1DA49-EC11-4068-9DC6-D721894371F9">WICDdsFormatInfo</a>
 

 

