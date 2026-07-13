---
UID: NN:xpsobjectmodel.IXpsOMMatrixTransform
title: IXpsOMMatrixTransform (xpsobjectmodel.h)
description: Specifies an affine matrix transform that can be applied to other objects in the object model.
helpviewer_keywords: ["IXpsOMMatrixTransform","IXpsOMMatrixTransform interface [XPS Documents and Packaging]","IXpsOMMatrixTransform interface [XPS Documents and Packaging]","described","xps.ixpsommatrixtransform","xpsobjectmodel/IXpsOMMatrixTransform"]
old-location: xps\ixpsommatrixtransform.htm
tech.root: xps
ms.assetid: d21457bc-9445-4ca2-ab9f-1e3f55e2e635
ms.date: 12/05/2018
ms.keywords: IXpsOMMatrixTransform, IXpsOMMatrixTransform interface [XPS Documents and Packaging], IXpsOMMatrixTransform interface [XPS Documents and Packaging],described, xps.ixpsommatrixtransform, xpsobjectmodel/IXpsOMMatrixTransform
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
 - IXpsOMMatrixTransform
 - xpsobjectmodel/IXpsOMMatrixTransform
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
 - IXpsOMMatrixTransform
---

# IXpsOMMatrixTransform interface

## -description

Specifies an affine matrix transform that can be applied to other objects in the object model.

## -inheritance

The <b>IXpsOMMatrixTransform</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>. <b>IXpsOMMatrixTransform</b> also has these types of members:

## -remarks

The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMMatrixTransform    *newInterface;
// The following value is defined outside of 
// this example.
XPS_MATRIX        newMatrix;

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
    hr = xpsFactory->CreateMatrixTransform (
        &newMatrix,
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

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creatematrixtransform">IXpsOMObjectFactory::CreateMatrixTransform</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a>
