---
UID: NN:xpsobjectmodel.IXpsOMImageResource
title: IXpsOMImageResource (xpsobjectmodel.h)
description: Provides an IStream interface to an image resource.
helpviewer_keywords: ["IXpsOMImageResource","IXpsOMImageResource interface [XPS Documents and Packaging]","IXpsOMImageResource interface [XPS Documents and Packaging]","described","xps.ixpsomimageresource","xpsobjectmodel/IXpsOMImageResource"]
old-location: xps\ixpsomimageresource.htm
tech.root: xps
ms.assetid: 89a1530e-fa87-45bf-a1da-c8656ec09ba3
ms.date: 12/05/2018
ms.keywords: IXpsOMImageResource, IXpsOMImageResource interface [XPS Documents and Packaging], IXpsOMImageResource interface [XPS Documents and Packaging],described, xps.ixpsomimageresource, xpsobjectmodel/IXpsOMImageResource
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
 - IXpsOMImageResource
 - xpsobjectmodel/IXpsOMImageResource
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
 - IXpsOMImageResource
---

# IXpsOMImageResource interface

## -description

Provides an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to an image resource.

## -inheritance

The <b>IXpsOMImageResource</b> interface inherits from <a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMImageResource</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMImageResource    *newInterface;
// The following values are defined outside of 
// this example.
//  IStream            *acquiredStream;
//  XPS_IMAGE_TYPE     contentType;
//  IOpcPartUri        *partUri;
    
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
    // The partUriString and acquiredStream variables 
    //   are defined outside of this example.
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreateImageResource (
            acquiredStream,
            contentType,
            partUri,
            &newInterface);
        if (SUCCEEDED(hr))
        {
            // use newInterface

            newInterface->Release();
        }
        partUri->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createimageresource">IXpsOMObjectFactory::CreateImageResource</a>



<a href="/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
