---
UID: NF:imagetranscode.ITranscodeImage.TranscodeImage
title: ITranscodeImage::TranscodeImage (imagetranscode.h)
description: Converts an image to JPEG or bitmap (BMP) image format.
helpviewer_keywords: ["ITranscodeImage interface [Windows Shell]","TranscodeImage method","ITranscodeImage.TranscodeImage","ITranscodeImage::TranscodeImage","TI_BITMAP","TI_JPEG","TranscodeImage","TranscodeImage method [Windows Shell]","TranscodeImage method [Windows Shell]","ITranscodeImage interface","_shell_TranscodeImage","imagetranscode/ITranscodeImage::TranscodeImage","shell.TranscodeImage"]
old-location: shell\TranscodeImage.htm
tech.root: shell
ms.assetid: 56b8c871-5c44-497d-beac-5bde01b8bd8b
ms.date: 12/05/2018
ms.keywords: ITranscodeImage interface [Windows Shell],TranscodeImage method, ITranscodeImage.TranscodeImage, ITranscodeImage::TranscodeImage, TI_BITMAP, TI_JPEG, TranscodeImage, TranscodeImage method [Windows Shell], TranscodeImage method [Windows Shell],ITranscodeImage interface, _shell_TranscodeImage, imagetranscode/ITranscodeImage::TranscodeImage, shell.TranscodeImage
req.header: imagetranscode.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITranscodeImage::TranscodeImage
 - imagetranscode/ITranscodeImage::TranscodeImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imagetranscode.h
api_name:
 - ITranscodeImage.TranscodeImage
---

# ITranscodeImage::TranscodeImage


## -description

Converts an image to JPEG or bitmap (BMP) image format.

## -parameters

### -param pShellItem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

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

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A stream to receive the converted image. The stream must be created by the calling code prior to calling <b>TranscodeImage</b>.

### -param puiWidth [out, optional]

Type: <b>UINT*</b>

The actual width of the converted image.

### -param puiHeight [out, optional]

Type: <b>UINT*</b>

The actual height of the converted image.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The aspect ratio of the original image is preserved. 
		The new image is resized so that it will fit into a box of width <i>uiMaxWidth</i> and height <i>uiMaxHeight</i>.
		

The image size will not be changed if the original image already fits in this bounding box.

If both uiMaxWidth and uiMaxHeight are zero, the returned image will be the same size as the original.