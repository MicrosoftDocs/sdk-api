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

# ITranscodeImage::TranscodeImage


## -description


Converts an image to JPEG or bitmap (BMP) image format.


## -parameters




### -param pShellItem [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

The Shell Item for the image to convert.


### -param uiMaxWidth

Type: <b>UINT</b>

The requested height in pixels. Should be less than or equal to the actual height of the original image. See Remarks.


### -param uiMaxHeight

Type: <b>UINT</b>

The requested width in pixels. Should be less than or equal to the actual width of the original image. See Remarks.


### -param flags

Type: <b>TI_FLAGS</b>

One of the following flags. 
				
				



#### TI_BITMAP

Convert the image to BMP format.



#### TI_JPEG

Convert the image to JPEG format.


### -param pvImage

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A stream to receive the converted image. The stream must be created by the calling code prior to calling <b>TranscodeImage</b>.


### -param puiWidth [out, optional]

Type: <b>UINT*</b>

The actual width of the converted image.


### -param puiHeight [out, optional]

Type: <b>UINT*</b>

The actual height of the converted image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The aspect ratio of the original image is preserved. 
		The new image is resized so that it will fit into a box of width <i>uiMaxWidth</i> and height <i>uiMaxHeight</i>.
		

The image size will not be changed if the original image already fits in this bounding box.

If both uiMaxWidth and uiMaxHeight are zero, the returned image will be the same size as the original.



