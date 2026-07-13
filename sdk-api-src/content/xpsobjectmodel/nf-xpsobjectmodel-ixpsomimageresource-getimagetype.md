---
UID: NF:xpsobjectmodel.IXpsOMImageResource.GetImageType
title: IXpsOMImageResource::GetImageType (xpsobjectmodel.h)
description: Gets the type of image resource.
helpviewer_keywords: ["GetImageType","GetImageType method [XPS Documents and Packaging]","GetImageType method [XPS Documents and Packaging]","IXpsOMImageResource interface","IXpsOMImageResource interface [XPS Documents and Packaging]","GetImageType method","IXpsOMImageResource.GetImageType","IXpsOMImageResource::GetImageType","xps.ixpsomimageresource_getimagetype","xpsobjectmodel/IXpsOMImageResource::GetImageType"]
old-location: xps\ixpsomimageresource_getimagetype.htm
tech.root: xps
ms.assetid: c38af0c0-e05c-4ba4-92d5-114350cae05f
ms.date: 12/05/2018
ms.keywords: GetImageType, GetImageType method [XPS Documents and Packaging], GetImageType method [XPS Documents and Packaging],IXpsOMImageResource interface, IXpsOMImageResource interface [XPS Documents and Packaging],GetImageType method, IXpsOMImageResource.GetImageType, IXpsOMImageResource::GetImageType, xps.ixpsomimageresource_getimagetype, xpsobjectmodel/IXpsOMImageResource::GetImageType
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - IXpsOMImageResource::GetImageType
 - xpsobjectmodel/IXpsOMImageResource::GetImageType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMImageResource.GetImageType
---

# IXpsOMImageResource::GetImageType


## -description

Gets the type of image resource.

## -parameters

### -param imageType [out, retval]

The  <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a> value that describes the image type in the stream.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource">IXpsOMImageResource</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type">XPS_IMAGE_TYPE</a>