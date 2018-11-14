---
UID: NF:wincodec.IWICDdsFrameDecode.GetSizeInBlocks
title: IWICDdsFrameDecode::GetSizeInBlocks
author: windows-sdk-content
description: Gets the width and height, in blocks, of the DDS image.
old-location: wic\iwicddsframedecode_getsizeinblocks.htm
tech.root: wic
ms.assetid: 34F3A19C-4B68-4E6A-AE08-71DE9A0687BF
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetSizeInBlocks, GetSizeInBlocks method [Windows Imaging Component], GetSizeInBlocks method [Windows Imaging Component],IWICDdsFrameDecode interface, IWICDdsFrameDecode interface [Windows Imaging Component],GetSizeInBlocks method, IWICDdsFrameDecode.GetSizeInBlocks, IWICDdsFrameDecode::GetSizeInBlocks, wic.iwicddsframedecode_getsizeinblocks, wincodec/IWICDdsFrameDecode::GetSizeInBlocks
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
 - IWICDdsFrameDecode.GetSizeInBlocks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICDdsFrameDecode.GetSizeInBlocks
: 
---

# IWICDdsFrameDecode::GetSizeInBlocks


## -description


Gets the width and height, in blocks, of the DDS image.


## -parameters




### -param pWidthInBlocks [out]

Type: <b>UINT*</b>

The width of the DDS image in blocks.


### -param pHeightInBlocks

TBD




#### - pHeight    InBlocks [out]

Type: <b>UINT*</b>

The height of the DDS image in blocks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For block compressed textures, the returned width and height values do not completely define the texture size because the image is padded to fit the closest whole block size. For example, three BC1 textures with pixel dimensions of 1x1, 2x2 and 4x4 will all report <i>pWidthInBlocks</i> = 1 and <i>pHeightInBlocks</i> = 1.



If the texture does not use a block-compressed <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>, this method returns the texture size in pixels; for these formats the block size returned by <a href="https://msdn.microsoft.com/0D5B9E45-E1EA-4D16-B793-63FEAB2BAF65">IWICDdsFrameDecoder::GetFormatInfo</a> is 1x1.





## -see-also




<a href="https://msdn.microsoft.com/52E76A8D-E7E2-46F5-BBCC-B7C74F1B1122">IWICDdsFrameDecode</a>
 

 

