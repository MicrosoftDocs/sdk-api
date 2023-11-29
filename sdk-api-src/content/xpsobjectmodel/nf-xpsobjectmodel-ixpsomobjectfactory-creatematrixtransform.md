---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateMatrixTransform
title: IXpsOMObjectFactory::CreateMatrixTransform (xpsobjectmodel.h)
description: Creates an IXpsOMMatrixTransform interface that specifies an affine matrix transform.
helpviewer_keywords: ["CreateMatrixTransform","CreateMatrixTransform method [XPS Documents and Packaging]","CreateMatrixTransform method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateMatrixTransform method","IXpsOMObjectFactory.CreateMatrixTransform","IXpsOMObjectFactory::CreateMatrixTransform","xps.ixpsomobjectfactory_creatematrixtransform","xpsobjectmodel/IXpsOMObjectFactory::CreateMatrixTransform"]
old-location: xps\ixpsomobjectfactory_creatematrixtransform.htm
tech.root: xps
ms.assetid: 10377a1f-67b4-4fae-81f7-e6bf50e1c2b2
ms.date: 12/05/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [XPS Documents and Packaging], CreateMatrixTransform method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateMatrixTransform method, IXpsOMObjectFactory.CreateMatrixTransform, IXpsOMObjectFactory::CreateMatrixTransform, xps.ixpsomobjectfactory_creatematrixtransform, xpsobjectmodel/IXpsOMObjectFactory::CreateMatrixTransform
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
 - IXpsOMObjectFactory::CreateMatrixTransform
 - xpsobjectmodel/IXpsOMObjectFactory::CreateMatrixTransform
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
 - IXpsOMObjectFactory.CreateMatrixTransform
---

# IXpsOMObjectFactory::CreateMatrixTransform


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that specifies an affine matrix transform.

## -parameters

### -param matrix [in]

The initial matrix to be assigned to the transform.

### -param transform [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>matrix</i> or <i>transform</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The transform specified by this matrix can be applied to the transform property of other XPS objects.

The code example that follows illustrates how this method is used to create a new  interface.


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a>