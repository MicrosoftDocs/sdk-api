---
UID: NN:xpsobjectmodel.IXpsOMPath
title: IXpsOMPath (xpsobjectmodel.h)
description: Describes a non-text visual item.
helpviewer_keywords: ["IXpsOMPath","IXpsOMPath interface [XPS Documents and Packaging]","IXpsOMPath interface [XPS Documents and Packaging]","described","xps.ixpsompath","xpsobjectmodel/IXpsOMPath"]
old-location: xps\ixpsompath.htm
tech.root: xps
ms.assetid: 93257a77-3fef-400e-bfe1-06e760ba4b93
ms.date: 12/05/2018
ms.keywords: IXpsOMPath, IXpsOMPath interface [XPS Documents and Packaging], IXpsOMPath interface [XPS Documents and Packaging],described, xps.ixpsompath, xpsobjectmodel/IXpsOMPath
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
 - IXpsOMPath
 - xpsobjectmodel/IXpsOMPath
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
 - IXpsOMPath
---

# IXpsOMPath interface

## -description

Describes a non-text visual item.

## -inheritance

The <b>IXpsOMPath</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>. <b>IXpsOMPath</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPath    *newInterface;

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
    hr = xpsFactory->CreatePath (&newInterface);

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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpath">IXpsOMObjectFactory::CreatePath</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
