---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateGeometryFigure
title: IXpsOMObjectFactory::CreateGeometryFigure (xpsobjectmodel.h)
description: Creates an IXpsOMGeometryFigure interface, which specifies a portion of an object that is defined by an IXpsOMGeometry interface.
helpviewer_keywords: ["CreateGeometryFigure","CreateGeometryFigure method [XPS Documents and Packaging]","CreateGeometryFigure method [XPS Documents and Packaging]","IXpsOMObjectFactory interface","IXpsOMObjectFactory interface [XPS Documents and Packaging]","CreateGeometryFigure method","IXpsOMObjectFactory.CreateGeometryFigure","IXpsOMObjectFactory::CreateGeometryFigure","xps.ixpsomobjectfactory_creategeometryfigure","xpsobjectmodel/IXpsOMObjectFactory::CreateGeometryFigure"]
old-location: xps\ixpsomobjectfactory_creategeometryfigure.htm
tech.root: xps
ms.assetid: d9138dbc-5a9e-4653-bab2-71f6d716eba6
ms.date: 12/05/2018
ms.keywords: CreateGeometryFigure, CreateGeometryFigure method [XPS Documents and Packaging], CreateGeometryFigure method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateGeometryFigure method, IXpsOMObjectFactory.CreateGeometryFigure, IXpsOMObjectFactory::CreateGeometryFigure, xps.ixpsomobjectfactory_creategeometryfigure, xpsobjectmodel/IXpsOMObjectFactory::CreateGeometryFigure
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
 - IXpsOMObjectFactory::CreateGeometryFigure
 - xpsobjectmodel/IXpsOMObjectFactory::CreateGeometryFigure
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
 - IXpsOMObjectFactory.CreateGeometryFigure
---

# IXpsOMObjectFactory::CreateGeometryFigure


## -description

Creates an  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface, which specifies a portion of an object that is defined by  an  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface.

## -parameters

### -param startPoint [in]

The coordinates of the starting point of the geometry figure.

### -param figure [out, retval]

A pointer to the new  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a> interface.

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
<i>startPoint</i> or <i>figure</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_FLOAT
</b></dt>
</dl>
</td>
<td width="60%">
One of the fields in the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure that is passed in <i>startPoint</i> contains a  value that is not valid.


</td>
</tr>
</table>

## -remarks

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMGeometryFigure    *newInterface;
// startPoint contains the starting point
// of the geometry figure being created
XPS_POINT                startPoint = {0,0};

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
    hr = xpsFactory->CreateGeometryFigure (&startPoint, &newInterface);
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory">IXpsOMObjectFactory</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>