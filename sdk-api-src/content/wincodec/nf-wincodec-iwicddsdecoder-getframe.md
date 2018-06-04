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
 

 

