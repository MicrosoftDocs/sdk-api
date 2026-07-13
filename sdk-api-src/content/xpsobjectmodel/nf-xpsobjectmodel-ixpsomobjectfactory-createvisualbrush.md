---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateVisualBrush
title: IXpsOMObjectFactory::CreateVisualBrush (xpsobjectmodel.h)
description: Creates an IXpsOMVisualBrush interface, which is an IXpsOMTileBrush that uses a visual object.
helpviewer_keywords: ["CreateVisualBrush","CreateVisualBrush method [XPS Documents and Packaging]","CreateVisualBrush method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateVisualBrush method","IXpsOMObjectFactory.CreateVisualBrush","IXpsOMObjectFactory::CreateVisualBrush","xps.ixpsomobjectfactory_createvisualbrush","xpsobjectmodel/IXpsOMObjectFactory::CreateVisualBrush"]
old-location: xps\ixpsomobjectfactory_createvisualbrush.htm
tech.root: xps
ms.assetid: ad19841a-629f-4127-a6ea-890168e0c53c
ms.date: 12/05/2018
ms.keywords: CreateVisualBrush, CreateVisualBrush method [XPS Documents and Packaging], CreateVisualBrush method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateVisualBrush method, IXpsOMObjectFactory.CreateVisualBrush, IXpsOMObjectFactory::CreateVisualBrush, xps.ixpsomobjectfactory_createvisualbrush, xpsobjectmodel/IXpsOMObjectFactory::CreateVisualBrush
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
 - IXpsOMObjectFactory::CreateVisualBrush
 - xpsobjectmodel/IXpsOMObjectFactory::CreateVisualBrush
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
 - IXpsOMObjectFactory.CreateVisualBrush
---

# IXpsOMObjectFactory::CreateVisualBrush


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a> interface, which is  an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>  that uses a visual object.

## -parameters

### -param viewBox [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a> structure that specifies the source image's  area to be used in the brush. This parameter must not be <b>NULL</b>.

### -param viewPort [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a> structure that specifies the destination geometry area of the tile. This parameter must not be <b>NULL</b>.

### -param visualBrush [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a> interface.

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
<i>viewBox</i>,  <i>viewPort</i>, or <i>visualBrush</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
<i>viewBox</i> or <i>viewPort</i> contains an invalid rectangle or value.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>