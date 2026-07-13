---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePartResources
title: IXpsOMObjectFactory::CreatePartResources (xpsobjectmodel.h)
description: Creates an IXpsOMPartResources interface that can contain part-based resources.
helpviewer_keywords: ["CreatePartResources","CreatePartResources method [XPS Documents and Packaging]","CreatePartResources method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreatePartResources method","IXpsOMObjectFactory.CreatePartResources","IXpsOMObjectFactory::CreatePartResources","xps.ixpsomobjectfactory_createpartresources","xpsobjectmodel/IXpsOMObjectFactory::CreatePartResources"]
old-location: xps\ixpsomobjectfactory_createpartresources.htm
tech.root: xps
ms.assetid: f525139b-a94f-41ee-966f-408079a9e676
ms.date: 12/05/2018
ms.keywords: CreatePartResources, CreatePartResources method [XPS Documents and Packaging], CreatePartResources method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePartResources method, IXpsOMObjectFactory.CreatePartResources, IXpsOMObjectFactory::CreatePartResources, xps.ixpsomobjectfactory_createpartresources, xpsobjectmodel/IXpsOMObjectFactory::CreatePartResources
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
 - IXpsOMObjectFactory::CreatePartResources
 - xpsobjectmodel/IXpsOMObjectFactory::CreatePartResources
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
 - IXpsOMObjectFactory.CreatePartResources
---

# IXpsOMObjectFactory::CreatePartResources


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface that can contain part-based resources.

## -parameters

### -param partResources [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a> interface.

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
<i>partResources</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The part resources are shared between pages of a document and can include fonts, images, color profiles, and remote dictionaries.

To find the part resources of a document, call  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources">IXpsOMPageReference::CollectPartResources</a>.

The code example that follows illustrates how this method is used to create a new  interface.


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources">IXpsOMPartResources</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>