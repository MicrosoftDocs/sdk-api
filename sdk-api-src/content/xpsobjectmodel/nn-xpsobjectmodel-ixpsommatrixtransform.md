---
UID: NN:xpsobjectmodel.IXpsOMMatrixTransform
title: IXpsOMMatrixTransform
author: windows-sdk-content
description: Specifies an affine matrix transform that can be applied to other objects in the object model.
old-location: xps\ixpsommatrixtransform.htm
tech.root: printdocs
ms.assetid: d21457bc-9445-4ca2-ab9f-1e3f55e2e635
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMMatrixTransform, IXpsOMMatrixTransform interface [XPS Documents and Packaging], IXpsOMMatrixTransform interface [XPS Documents and Packaging],described, xps.ixpsommatrixtransform, xpsobjectmodel/IXpsOMMatrixTransform
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMMatrixTransform interface


## -description


Specifies an affine matrix transform that can be applied to other objects in the object model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMMatrixTransform</b> interface inherits from <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>. <b>IXpsOMMatrixTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/088e758c-5839-4560-955c-98c8a1ee99ae">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4067778d-d10f-4b53-9419-f438b7197f44">GetMatrix</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure, which specifies the transform matrix.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbe6a992-1c94-40b0-a0b6-3b214b928805">SetMatrix</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure, which specifies the transform matrix.
            

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreateMatrixTransform (
        &amp;newMatrix,
        &amp;newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface-&gt;Release();
    }
    xpsFactory-&gt;Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/10377a1f-67b4-4fae-81f7-e6bf50e1c2b2">IXpsOMObjectFactory::CreateMatrixTransform</a>



<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a>
 

 

