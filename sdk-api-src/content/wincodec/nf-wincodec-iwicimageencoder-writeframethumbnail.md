---
UID: NF:wincodec.IWICImageEncoder.WriteFrameThumbnail
title: IWICImageEncoder::WriteFrameThumbnail
author: windows-driver-content
description: Encodes the image as a thumbnail to the frame given by the IWICBitmapFrameEncode.
old-location: wic\iwicimageencoder_writeframethumbnail.htm
old-project: wic
ms.assetid: 5A34F900-73F1-4FFC-B251-F22E0EDDB873
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICImageEncoder interface [Windows Imaging Component],WriteFrameThumbnail method, IWICImageEncoder.WriteFrameThumbnail, IWICImageEncoder::WriteFrameThumbnail, WriteFrameThumbnail, WriteFrameThumbnail method [Windows Imaging Component], WriteFrameThumbnail method [Windows Imaging Component],IWICImageEncoder interface, wic.iwicimageencoder_writeframethumbnail, wincodec/IWICImageEncoder::WriteFrameThumbnail
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICImageEncoder.WriteFrameThumbnail
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImageEncoder::WriteFrameThumbnail


## -description


Encodes the image as a thumbnail to the frame given by the <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a>. 


## -parameters




### -param pImage [in]

Type: <b><a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.


### -param pFrameEncode [in]

Type: <b><a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a>*</b>

The frame encoder on which the thumbnail is set.


### -param pImageParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/0B461697-C7ED-48C9-A880-1B5F4A26FCFC">WICImageParameters</a>*</b>

Additional parameters to control encoding.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The image passed in must be created on the same device as in <a href="https://msdn.microsoft.com/1F75030F-68B0-4333-B3CF-C4ABD8969448">IWICImagingFactory2::CreateImageEncoder</a>. If the <i>pImageParameters</i> are not specified, a set of useful defaults will be assumed, see <a href="https://msdn.microsoft.com/0B461697-C7ED-48C9-A880-1B5F4A26FCFC">WICImageParameters</a> for more info.



You must correctly and independently have set up the <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a> before calling this API.





## -see-also




<a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a>
 

 

