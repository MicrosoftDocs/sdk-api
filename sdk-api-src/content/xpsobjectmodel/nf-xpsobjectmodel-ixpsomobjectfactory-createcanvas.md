---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateCanvas
title: IXpsOMObjectFactory::CreateCanvas (xpsobjectmodel.h)
description: Creates an IXpsOMCanvas interface that is used to group page elements.
helpviewer_keywords: ["CreateCanvas","CreateCanvas method [XPS Documents and Packaging]","CreateCanvas method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateCanvas method","IXpsOMObjectFactory.CreateCanvas","IXpsOMObjectFactory::CreateCanvas","xps.ixpsomobjectfactory_createcanvas","xpsobjectmodel/IXpsOMObjectFactory::CreateCanvas"]
old-location: xps\ixpsomobjectfactory_createcanvas.htm
tech.root: xps
ms.assetid: 1ee3a80d-f6d8-45ba-8178-e3870404698a
ms.date: 12/05/2018
ms.keywords: CreateCanvas, CreateCanvas method [XPS Documents and Packaging], CreateCanvas method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateCanvas method, IXpsOMObjectFactory.CreateCanvas, IXpsOMObjectFactory::CreateCanvas, xps.ixpsomobjectfactory_createcanvas, xpsobjectmodel/IXpsOMObjectFactory::CreateCanvas
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
 - IXpsOMObjectFactory::CreateCanvas
 - xpsobjectmodel/IXpsOMObjectFactory::CreateCanvas
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
 - IXpsOMObjectFactory.CreateCanvas
---

# IXpsOMObjectFactory::CreateCanvas


## -description

Creates an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a> interface that is used to group page elements.

## -parameters

### -param canvas [out, retval]

A pointer to the new <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a> interface.

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
<i>canvas</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMCanvas    *newInterface;

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
    hr = xpsFactory->CreateCanvas (&newInterface);
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas">IXpsOMCanvas</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>