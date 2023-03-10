---
UID: NF:xpsobjectmodel_1.IXpsOMObjectFactory1.ConvertJpegXRToHDPhoto
title: IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto (xpsobjectmodel_1.h)
description: Converts an image resource from a JpegXR to an HD Photo.
helpviewer_keywords: ["ConvertJpegXRToHDPhoto","ConvertJpegXRToHDPhoto method [XPS Documents and Packaging]","ConvertJpegXRToHDPhoto method [XPS Documents and Packaging]","IXpsOMObjectFactory1 interface","IXpsOMObjectFactory1 interface [XPS Documents and Packaging]","ConvertJpegXRToHDPhoto method","IXpsOMObjectFactory1.ConvertJpegXRToHDPhoto","IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto","xps.ixpsomobjectfactory1_convertjpegxrtohdphoto","xpsobjectmodel_1/IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto"]
old-location: xps\ixpsomobjectfactory1_convertjpegxrtohdphoto.htm
tech.root: xps
ms.assetid: 98cb0eca-229e-4224-bc9c-605f56cc298b
ms.date: 12/05/2018
ms.keywords: ConvertJpegXRToHDPhoto, ConvertJpegXRToHDPhoto method [XPS Documents and Packaging], ConvertJpegXRToHDPhoto method [XPS Documents and Packaging],IXpsOMObjectFactory1 interface, IXpsOMObjectFactory1 interface [XPS Documents and Packaging],ConvertJpegXRToHDPhoto method, IXpsOMObjectFactory1.ConvertJpegXRToHDPhoto, IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto, xps.ixpsomobjectfactory1_convertjpegxrtohdphoto, xpsobjectmodel_1/IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto
 - xpsobjectmodel_1/IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMObjectFactory1.ConvertJpegXRToHDPhoto
---

# IXpsOMObjectFactory1::ConvertJpegXRToHDPhoto


## -description

Converts an image resource from a JpegXR to an HD Photo.

## -parameters

### -param imageResource

[in, out] The image resource to convert. 

When the method returns, the converted image resource.

## -returns

Possible values include, but are not limited to, the following. For information about XPS document API return values that are not listed here, see XPS Document Errors.

S_OK: The method succeeded. 

XPS_E_INVALID_CONTENT_TYPE: The image type is not XPS_IMAGE_TYPE_JXR.

E_INVALIDARG if data is not recognized by WDP decoder or another error occurred.

## -remarks

This image referenced by imageResource is changed from an XPS_IMAGE_TYPE_JPEGXR image type to an XPS_IMAGE_TYPE_WDP image type. This method converts the data stream of the image resource;, however, the part name of the resource remains the same.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1">IXpsOMObjectFactory1</a>