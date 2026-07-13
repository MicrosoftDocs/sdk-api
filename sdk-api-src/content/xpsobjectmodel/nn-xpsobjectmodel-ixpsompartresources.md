---
UID: NN:xpsobjectmodel.IXpsOMPartResources
title: IXpsOMPartResources (xpsobjectmodel.h)
description: Provides access to all shared, part-based resources of the XPS document.
helpviewer_keywords: ["IXpsOMPartResources","IXpsOMPartResources interface [XPS Documents and Packaging]","IXpsOMPartResources interface [XPS Documents and Packaging]","described","xps.ixpsompartresources","xpsobjectmodel/IXpsOMPartResources"]
old-location: xps\ixpsompartresources.htm
tech.root: xps
ms.assetid: 9f706f23-25a0-40ee-93f4-3d7ac98ad6ed
ms.date: 12/05/2018
ms.keywords: IXpsOMPartResources, IXpsOMPartResources interface [XPS Documents and Packaging], IXpsOMPartResources interface [XPS Documents and Packaging],described, xps.ixpsompartresources, xpsobjectmodel/IXpsOMPartResources
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
 - IXpsOMPartResources
 - xpsobjectmodel/IXpsOMPartResources
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
 - IXpsOMPartResources
---

# IXpsOMPartResources interface

## -description

Provides access to all shared, part-based resources of the XPS document.

## -inheritance

The <b>IXpsOMPartResources</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXpsOMPartResources</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPartResources    *newInterface;

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
    hr = xpsFactory->CreatePartResources (&newInterface);

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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpartresources">IXpsOMObjectFactory::CreatePartResources</a>


<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
 

 

