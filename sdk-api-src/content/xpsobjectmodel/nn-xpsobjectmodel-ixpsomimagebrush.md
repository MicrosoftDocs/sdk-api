---
UID: NN:xpsobjectmodel.IXpsOMImageBrush
title: IXpsOMImageBrush (xpsobjectmodel.h)
description: A brush that uses a raster image as a source.
helpviewer_keywords: ["IXpsOMImageBrush","IXpsOMImageBrush interface [XPS Documents and Packaging]","IXpsOMImageBrush interface [XPS Documents and Packaging]","described","xps.ixpsomimagebrush","xpsobjectmodel/IXpsOMImageBrush"]
old-location: xps\ixpsomimagebrush.htm
tech.root: xps
ms.assetid: f5478582-466b-496e-b7f3-42fb8caa6814
ms.date: 12/05/2018
ms.keywords: IXpsOMImageBrush, IXpsOMImageBrush interface [XPS Documents and Packaging], IXpsOMImageBrush interface [XPS Documents and Packaging],described, xps.ixpsomimagebrush, xpsobjectmodel/IXpsOMImageBrush
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
 - IXpsOMImageBrush
 - xpsobjectmodel/IXpsOMImageBrush
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
 - IXpsOMImageBrush
---

# IXpsOMImageBrush interface

## -description

A brush that uses a raster image as a source.

## -inheritance

The <b>IXpsOMImageBrush</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>. <b>IXpsOMImageBrush</b> also has these types of members:

## -remarks

The image used by this brush is defined in a coordinate space that is specified by the image's resolution. The image type must be JPEG, PNG, TIFF 6.0, or HD  Photo.

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMImageBrush            *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMImageResource     *image;
//  XPS_RECT                viewBox;
//  XPS_RECT                viewPort;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreateImageBrush (
        image,
        &viewBox,
        &viewPort,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createimagebrush">IXpsOMObjectFactory::CreateImageBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
