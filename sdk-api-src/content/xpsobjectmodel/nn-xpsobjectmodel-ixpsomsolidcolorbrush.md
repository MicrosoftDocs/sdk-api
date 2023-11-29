---
UID: NN:xpsobjectmodel.IXpsOMSolidColorBrush
title: IXpsOMSolidColorBrush (xpsobjectmodel.h)
description: A single-color brush.
helpviewer_keywords: ["IXpsOMSolidColorBrush","IXpsOMSolidColorBrush interface [XPS Documents and Packaging]","IXpsOMSolidColorBrush interface [XPS Documents and Packaging]","described","xps.ixpsomsolidcolorbrush","xpsobjectmodel/IXpsOMSolidColorBrush"]
old-location: xps\ixpsomsolidcolorbrush.htm
tech.root: xps
ms.assetid: 26580a25-09d1-4a9b-85c3-aa8ddcc97867
ms.date: 12/05/2018
ms.keywords: IXpsOMSolidColorBrush, IXpsOMSolidColorBrush interface [XPS Documents and Packaging], IXpsOMSolidColorBrush interface [XPS Documents and Packaging],described, xps.ixpsomsolidcolorbrush, xpsobjectmodel/IXpsOMSolidColorBrush
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
 - IXpsOMSolidColorBrush
 - xpsobjectmodel/IXpsOMSolidColorBrush
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
 - IXpsOMSolidColorBrush
---

# IXpsOMSolidColorBrush interface

## -description

A  single-color brush.

## -inheritance

The <b>IXpsOMSolidColorBrush</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>. <b>IXpsOMSolidColorBrush</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMSolidColorBrush             *newInterface;
// The following values are defined outside of 
// this example.
//  XPS_COLOR                     color;
//  IXpsOMColorProfileResource    *colorProfile;

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
    hr = xpsFactory->CreateSolidColorBrush (
        &color,
        colorProfile,
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createsolidcolorbrush">IXpsOMObjectFactory::CreateSolidColorBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createsolidcolorbrush">IXpsOMObjectFactory::CreateSolidColorBrush</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
 

 

