---
UID: NN:xpsobjectmodel.IXpsOMGeometryFigure
title: IXpsOMGeometryFigure (xpsobjectmodel.h)
description: Describes one portion of the path or clipping region that is specified by an IXpsOMGeometry interface.
helpviewer_keywords: ["IXpsOMGeometryFigure","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","described","xps.ixpsomgeometryfigure","xpsobjectmodel/IXpsOMGeometryFigure"]
old-location: xps\ixpsomgeometryfigure.htm
tech.root: xps
ms.assetid: e76a14ce-cfc3-4a50-855e-f5779b9fc261
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometryFigure, IXpsOMGeometryFigure interface [XPS Documents and Packaging], IXpsOMGeometryFigure interface [XPS Documents and Packaging],described, xps.ixpsomgeometryfigure, xpsobjectmodel/IXpsOMGeometryFigure
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
 - IXpsOMGeometryFigure
 - xpsobjectmodel/IXpsOMGeometryFigure
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
 - IXpsOMGeometryFigure
---

# IXpsOMGeometryFigure interface

## -description

Describes one portion of the path or clipping region that is specified by an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface.

## -inheritance

The <b>IXpsOMGeometryFigure</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMGeometryFigure</b> also has these types of members:

## -remarks

The <b>IXpsOMGeometryFigure</b> corresponds to the <b>PathFigure</b> element in XPS markup.

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMGeometryFigure    *newInterface;
// startPoint contains the starting point
// of the geometry figure being created
XPS_POINT                startPoint = {0,0};

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
    hr = xpsFactory->CreateGeometryFigure (&startPoint, &newInterface);
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creategeometryfigure">IXpsOMObjectFactory::CreateGeometryFigure</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_stroke_pattern">XPS_SEGMENT_STROKE_PATTERN</a>
