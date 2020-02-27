---
UID: NN:xpsobjectmodel.IXpsOMMatrixTransform
title: IXpsOMMatrixTransform (xpsobjectmodel.h)
description: Specifies an affine matrix transform that can be applied to other objects in the object model.
old-location: xps\ixpsommatrixtransform.htm
tech.root: printdocs
ms.assetid: d21457bc-9445-4ca2-ab9f-1e3f55e2e635
ms.date: 12/05/2018
ms.keywords: IXpsOMMatrixTransform, IXpsOMMatrixTransform interface [XPS Documents and Packaging], IXpsOMMatrixTransform interface [XPS Documents and Packaging],described, xps.ixpsommatrixtransform, xpsobjectmodel/IXpsOMMatrixTransform
f1_keywords:
- xpsobjectmodel/IXpsOMMatrixTransform
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xpsobjectmodel.h
api_name:
- IXpsOMMatrixTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMMatrixTransform interface


## -description


Specifies an affine matrix transform that can be applied to other objects in the object model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMMatrixTransform</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>. <b>IXpsOMMatrixTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMMatrixTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsommatrixtransform-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsommatrixtransform-getmatrix">GetMatrix</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a> structure, which specifies the transform matrix.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsommatrixtransform-setmatrix">SetMatrix</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a> structure, which specifies the transform matrix.
            

</td>
</tr>
</table> 


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




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-creatematrixtransform">IXpsOMObjectFactory::CreateMatrixTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>



<a href="https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a>
 

 

