---
UID: NN:xpsobjectmodel.IXpsOMDocument
title: IXpsOMDocument (xpsobjectmodel.h)
description: An ordered sequence of fixed pages and document-level resources that make up the document.
helpviewer_keywords: ["IXpsOMDocument","IXpsOMDocument interface [XPS Documents and Packaging]","IXpsOMDocument interface [XPS Documents and Packaging]","described","xps.ixpsomdocument","xpsobjectmodel/IXpsOMDocument"]
old-location: xps\ixpsomdocument.htm
tech.root: xps
ms.assetid: 22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f
ms.date: 12/05/2018
ms.keywords: IXpsOMDocument, IXpsOMDocument interface [XPS Documents and Packaging], IXpsOMDocument interface [XPS Documents and Packaging],described, xps.ixpsomdocument, xpsobjectmodel/IXpsOMDocument
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
 - IXpsOMDocument
 - xpsobjectmodel/IXpsOMDocument
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
 - IXpsOMDocument
---

# IXpsOMDocument interface

## -description

An ordered sequence of fixed pages and document-level resources that make up the document.

## -inheritance

The <b>IXpsOMDocument</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>. <b>IXpsOMDocument</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMDocument    *newInterface;
IOpcPartUri       *partUri;

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
    hr = xpsFactory->CreatePartUri(partUriString, &partUri);
    
    if (SUCCEEDED(hr))
    {
        hr = xpsFactory->CreateDocument (partUri, &newInterface);
        
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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createdocument">IXpsOMObjectFactory::CreateDocument</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart">IXpsOMPart</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
