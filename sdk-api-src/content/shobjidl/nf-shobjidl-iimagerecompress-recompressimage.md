---
UID: NF:shobjidl.IImageRecompress.RecompressImage
title: IImageRecompress::RecompressImage
author: windows-sdk-content
description: Recompresses an image. Implemented in an ImageRecompress object, this method accepts x and y dimensions with a designation of quality. The method creates a stream containing the new image that has been recompressed to the specified size.
old-location: shell\IImageRecompress_RecompressImage.htm
tech.root: shell
ms.assetid: 5fc215b0-c670-4287-8b6d-9fd6345b6439
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IImageRecompress interface [Windows Shell],RecompressImage method, IImageRecompress.RecompressImage, IImageRecompress::RecompressImage, RecompressImage, RecompressImage method [Windows Shell], RecompressImage method [Windows Shell],IImageRecompress interface, _win32_IImageRecompress_RecompressImage, shell.IImageRecompress_RecompressImage, shobjidl/IImageRecompress::RecompressImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shimgvw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shimgvw.dll
api_name:
 - IImageRecompress.RecompressImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImageRecompress::RecompressImage


## -description


Recompresses an image. Implemented in an
		<a href="https://msdn.microsoft.com/2eb4568f-e51a-4fdf-b78e-ca37af9ef86e">ImageRecompress</a> object, this method
		accepts x and y dimensions with a designation of quality. The method
		creates a stream containing the new image that has been recompressed
		to the	specified size.


## -parameters




### -param psi [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the object containing the stream of the image to read.


### -param cx [in]

Type: <b>int</b>

The x dimension of the image to return.


### -param cy [in]

Type: <b>int</b>

The y dimension of the image to return.


### -param iQuality [in]

Type: <b>int</b>

An indication of recompression quality that can range from 0 to 100.


### -param pstg [in]

Type: <b><a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the
				object that contains the stream to be written to.


### -param ppstrmOut [in, out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

The address of an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointer
				variable that receives the output stream written to.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.
				If the image in the input stream is less than the size specified by
				<i>cx</i> and
				<i>cy</i>,
				then S_FALSE is returned.




## -see-also




<a href="https://msdn.microsoft.com/48e07bc4-da70-406b-8024-3fa36416247f">IImageRecompress</a>



<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>



<a href="https://msdn.microsoft.com/2eb4568f-e51a-4fdf-b78e-ca37af9ef86e">ImageRecompress</a>
 

 

