---
UID: NN:xpsobjectmodel.IXpsOMGeometry
title: IXpsOMGeometry (xpsobjectmodel.h)
description: Describes the shape of a path or of a clipping region.
helpviewer_keywords: ["IXpsOMGeometry","IXpsOMGeometry interface [XPS Documents and Packaging]","IXpsOMGeometry interface [XPS Documents and Packaging]","described","xps.ixpsomgeometry","xpsobjectmodel/IXpsOMGeometry"]
old-location: xps\ixpsomgeometry.htm
tech.root: xps
ms.assetid: d3f74c1e-49ef-40ee-a2f4-b6d198b57624
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometry, IXpsOMGeometry interface [XPS Documents and Packaging], IXpsOMGeometry interface [XPS Documents and Packaging],described, xps.ixpsomgeometry, xpsobjectmodel/IXpsOMGeometry
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
 - IXpsOMGeometry
 - xpsobjectmodel/IXpsOMGeometry
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
 - IXpsOMGeometry
---

# IXpsOMGeometry interface

## -description

Describes the shape of a path or of a clipping region.

## -inheritance

The <b>IXpsOMGeometry</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>. <b>IXpsOMGeometry</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMGeometry    *newInterface;

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
    hr = xpsFactory->CreateGeometry (&newInterface);
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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategeometry">IXpsOMObjectFactory::CreateGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
