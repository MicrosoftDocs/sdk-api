---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateRadialGradientBrush
title: IXpsOMObjectFactory::CreateRadialGradientBrush
author: windows-sdk-content
description: Creates an IXpsOMRadialGradientBrush interface.
old-location: xps\ixpsomobjectfactory_createradialgradientbrush.htm
old-project: printdocs
ms.assetid: b91c9490-1995-48cb-a313-ef83f00b9c50
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush method [XPS Documents and Packaging], CreateRadialGradientBrush method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateRadialGradientBrush method, IXpsOMObjectFactory.CreateRadialGradientBrush, IXpsOMObjectFactory::CreateRadialGradientBrush, xps.ixpsomobjectfactory_createradialgradientbrush, xpsobjectmodel/IXpsOMObjectFactory::CreateRadialGradientBrush
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMObjectFactory.CreateRadialGradientBrush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreateRadialGradientBrush


## -description


Creates an <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a> interface.


## -parameters




### -param gradStop1 [in]

The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface that specifies the  properties of the gradient  at gradient origin. This parameter must not be <b>NULL</b>.


### -param gradStop2 [in]

The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface that specifies the  properties of the gradient  at the end of  the gradient's vector, which is the ellipse that encloses the gradient region. This parameter must not be <b>NULL</b>.


### -param centerPoint [in]

The coordinates of the center point of the radial gradient ellipse.


### -param gradientOrigin [in]

The coordinates of the origin  of the radial gradient.




### -param radiiSizes [in]

The <a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> structure whose members specify the lengths of the gradient region's radii.

Size is described in XPS units. There are 96 XPS units per inch. For example, a 1" radius is 96 XPS units.

<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> Member</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>width</b>

</td>
<td>
Length of the radius  along the x-axis.

</td>
</tr>
<tr>
<td>
<b>height</b>

</td>
<td>
Length of the radius  along the y-axis.

</td>
</tr>
</table>
 


### -param radialGradientBrush [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a> interface.


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
The point that is described by <i>centerPoint</i>, <i>radiiSizes</i>, or <i>gradientOrigin</i> is not valid. The members of the <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure must contain valid and finite floating-point values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>gradStop1</i>,  <i>gradStop2</i>, <i>centerPoint</i>, <i>gradientOrigin</i>, <i>radiiSizes</i>, or <i>radialGradientBrush</i> is <b>NULL</b>.

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



  As shown in the following illustration, the gradient region of a radial gradient is the area enclosed by the ellipse that is described by the center point and the x and y radii that extend from the center point. The spread area is the area outside of that ellipse. The gradient path (not shown) is a radial line that is drawn between the gradient origin and the ellipse that bounds the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>
For radial-gradient brushes, the gradient stop that is set by the <i>gradStop1</i> parameter corresponds to the gradient origin location and an offset value of 0.0. The gradient stop that is set by the <i>gradStop2</i> parameter corresponds to the circumference of the gradient region and an offset value of 1.0. For more information on gradient stops, see <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>.

The code example that follows illustrates how this method is used to create a new  interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMRadialGradientBrush    *newInterface;
// The following values are defined outside of 
// this example.
//  IXpsOMGradientStop       *gradStop1, *gradStop2;
//  XPS_POINT                centerPoint, gradientOrigin;
//  XPS_SIZE                 radiiSizes;

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
    hr = xpsFactory-&gt;CreateRadialGradientBrush (
        gradStop1,
        gradStop2,
        &amp;centerPoint,
        &amp;gradientOrigin,
        &amp;radiiSizes,
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



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>



<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a>
 

 

