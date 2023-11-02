---
UID: NN:xpsobjectmodel.IXpsOMVisualBrush
title: IXpsOMVisualBrush (xpsobjectmodel.h)
description: A brush that uses a visual element as a source.
helpviewer_keywords: ["IXpsOMVisualBrush","IXpsOMVisualBrush interface [XPS Documents and Packaging]","IXpsOMVisualBrush interface [XPS Documents and Packaging]","described","xps.ixpsomvisualbrush","xpsobjectmodel/IXpsOMVisualBrush"]
old-location: xps\ixpsomvisualbrush.htm
tech.root: xps
ms.assetid: 56c11e64-64a8-4c42-9547-4f1fcdc13a4b
ms.date: 12/05/2018
ms.keywords: IXpsOMVisualBrush, IXpsOMVisualBrush interface [XPS Documents and Packaging], IXpsOMVisualBrush interface [XPS Documents and Packaging],described, xps.ixpsomvisualbrush, xpsobjectmodel/IXpsOMVisualBrush
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
 - IXpsOMVisualBrush
 - xpsobjectmodel/IXpsOMVisualBrush
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
 - IXpsOMVisualBrush
---

# IXpsOMVisualBrush interface

## -description

A brush that uses a visual element as a source.

## -inheritance

The <b>IXpsOMVisualBrush</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>. <b>IXpsOMVisualBrush</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMVisualBrush        *newInterface;

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
    hr = xpsFactory->CreateVisualBrush (
        &viewBox,
        &viewPort,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // assign visual using one of the following:
        newInterface->SetVisualLocal (localVisual);
        // or
        newInterface->SetVisualLookup (visualLookupKey);
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
// use newInterface

newInterface->Release();
xpsFactory->Release();


```

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createvisualbrush">IXpsOMObjectFactory::CreateVisualBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
