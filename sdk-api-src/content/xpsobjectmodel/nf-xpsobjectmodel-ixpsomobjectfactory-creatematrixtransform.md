---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateMatrixTransform
title: IXpsOMObjectFactory::CreateMatrixTransform
author: windows-sdk-content
description: Creates an IXpsOMMatrixTransform interface that specifies an affine matrix transform.
old-location: xps\ixpsomobjectfactory_creatematrixtransform.htm
tech.root: printdocs
ms.assetid: 10377a1f-67b4-4fae-81f7-e6bf50e1c2b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [XPS Documents and Packaging], CreateMatrixTransform method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateMatrixTransform method, IXpsOMObjectFactory.CreateMatrixTransform, IXpsOMObjectFactory::CreateMatrixTransform, xps.ixpsomobjectfactory_creatematrixtransform, xpsobjectmodel/IXpsOMObjectFactory::CreateMatrixTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXpsOMObjectFactory.CreateMatrixTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreateMatrixTransform


## -description


Creates an <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that specifies an affine matrix transform.


## -parameters




### -param matrix [in]

The initial matrix to be assigned to the transform.


### -param transform [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a>
 

 

