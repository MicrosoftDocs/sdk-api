---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateLinearGradientBrush
title: IXpsOMObjectFactory::CreateLinearGradientBrush
author: windows-driver-content
description: Creates an IXpsOMLinearGradientBrush interface.
old-location: xps\ixpsomobjectfactory_createlineargradientbrush.htm
old-project: printdocs
ms.assetid: b829e8fe-5ef0-43d8-b115-9cddbfe1a255
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreateLinearGradientBrush, CreateLinearGradientBrush method [XPS Documents and Packaging], CreateLinearGradientBrush method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateLinearGradientBrush method, IXpsOMObjectFactory.CreateLinearGradientBrush, IXpsOMObjectFactory::CreateLinearGradientBrush, xps.ixpsomobjectfactory_createlineargradientbrush, xpsobjectmodel/IXpsOMObjectFactory::CreateLinearGradientBrush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMObjectFactory.CreateLinearGradientBrush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreateLinearGradientBrush


## -description


Creates an <a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a> interface.


## -parameters




### -param gradStop1 [in]


            The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface that specifies the  gradient properties at  the beginning of  the gradient's vector. This parameter must not be <b>NULL</b>.


### -param gradStop2 [in]

The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface that specifies the  gradient properties at the end of the gradient's vector. This parameter must not be <b>NULL</b>.


### -param startPoint [in]

The <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure that contains the coordinates of the start point in two-dimensional space.


### -param endPoint [in]

The <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure that contains the coordinates of the end point in two-dimensional space.


### -param linearGradientBrush [out, retval]


            A pointer to the new <a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a> interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The point specified by either <i>startPoint</i> or <i>endPoint</i> was not valid. The members of the <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure must contain valid and finite floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>gradStop1</i>, <i>gradStop2</i>, <i>startPoint</i>, <i>figure</i>, or <i>linearGradientBrush</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>gradStop1</i>  or <i>gradStop1</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



The gradient region of a linear gradient is the area between and including the start and end points and extending in both directions at a right angle to the gradient path. The spread area is the area of the geometry that lies outside the gradient region.

Gradient stops define the color at specific locations along the gradient path. In the illustration, gradient stop 0, specified by the <i>gradStop1</i> parameter,  is located at the start point of the gradient path, and gradient stop 1, specified by the  <i>gradStop2</i> parameter, is at the end point.

As shown in the illustration that follows, the start and end points of a linear gradient are also the start and end points of the gradient path, which is the straight line that connects those points.

<img alt="A figure that shows the terms used in a linear gradient" src="../images/LinearGradient1.png"/>
The code example that follows illustrates how this method is used to create a new  interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMLinearGradientBrush    *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMGradientStop       *gradStop1, *gradStop2;
//  XPS_POINT                startPoint, endPoint;

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
    hr = xpsFactory-&gt;CreateLinearGradientBrush (
        gradStop1,
        gradStop2,
        &amp;startPoint,
        &amp;endPoint,
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




<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

