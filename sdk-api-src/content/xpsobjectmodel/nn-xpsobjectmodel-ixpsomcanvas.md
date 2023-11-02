---
UID: NN:xpsobjectmodel.IXpsOMCanvas
title: IXpsOMCanvas (xpsobjectmodel.h)
description: A group of visual elements and related properties.
helpviewer_keywords: ["IXpsOMCanvas","IXpsOMCanvas interface [XPS Documents and Packaging]","IXpsOMCanvas interface [XPS Documents and Packaging]","described","xps.ixpsomcanvas","xpsobjectmodel/IXpsOMCanvas"]
old-location: xps\ixpsomcanvas.htm
tech.root: xps
ms.assetid: 3cb0e1b3-88a8-4724-a3c5-0df416294e62
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas, IXpsOMCanvas interface [XPS Documents and Packaging], IXpsOMCanvas interface [XPS Documents and Packaging],described, xps.ixpsomcanvas, xpsobjectmodel/IXpsOMCanvas
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
 - IXpsOMCanvas
 - xpsobjectmodel/IXpsOMCanvas
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
 - IXpsOMCanvas
---

# IXpsOMCanvas interface

## -description

A group of visual elements and related properties.

## -inheritance

The <b>IXpsOMCanvas</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>. <b>IXpsOMCanvas</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMCanvas    *newInterface;

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
    hr = xpsFactory->CreateCanvas (&newInterface);
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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createcanvas">IXpsOMObjectFactory::CreateCanvas</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
