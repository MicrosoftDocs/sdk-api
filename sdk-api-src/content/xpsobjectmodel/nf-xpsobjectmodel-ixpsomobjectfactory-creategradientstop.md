---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreateGradientStop
title: IXpsOMObjectFactory::CreateGradientStop
author: windows-sdk-content
description: Creates an IXpsOMGradientStop interface to represent a single color and location definition within a gradient.
old-location: xps\ixpsomobjectfactory_creategradientstop.htm
old-project: printdocs
ms.assetid: c9217444-fc9d-4b1e-abb2-7e1badd32052
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateGradientStop, CreateGradientStop method [XPS Documents and Packaging], CreateGradientStop method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreateGradientStop method, IXpsOMObjectFactory.CreateGradientStop, IXpsOMObjectFactory::CreateGradientStop, xps.ixpsomobjectfactory_creategradientstop, xpsobjectmodel/IXpsOMObjectFactory::CreateGradientStop
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMObjectFactory.CreateGradientStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreateGradientStop


## -description


Creates an <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface to represent a single color and location definition within a gradient.


## -parameters




### -param color [in]

The color value.


### -param colorProfile [in]

A pointer to the <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface that contains the color profile to be used. If the color type is not <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>, this parameter must be <b>NULL</b>.


### -param offset [in]

The offset value.

Valid range: 0.0–1.0




### -param gradientStop [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface.


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
The value in <i>offset</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>color</i> or <i>gradientStop</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MISSING_COLORPROFILE</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> is <b>NULL</b> but a color profile is expected. A color profile is required when the color type is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_UNEXPECTED_COLORPROFILE</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> contains a color profile but one is not expected. A color profile is only allowed when the color type is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>.

</td>
</tr>
</table>
 




## -remarks



 Gradient stops are used to define the color at a specific location; the color is interpolated between the gradient stops. The offset, which is specified by <i>offset</i>,  is a relative position between the start  and end points of the gradient. The  offset at the start point of a linear gradient or the origin of a radial  gradient is 0.0.  The offset of the end point of a linear gradient or the  bounding ellipse of a radial gradient is 1.0. Gradient stops can be specified for any offset between those points, including the start and end points. The following illustration shows the gradient path and gradient stops of a linear gradient.

<img alt="A figure that shows the terms used in a linear gradient" src="../images/LinearGradient2.png"/>
The following illustration shows the gradient stops of a radial gradient. In this example, the radial gradient region is the area enclosed by the outer ellipse and the <b>XPS_SPREAD_METHOD_REFLECT</b> spread method  is used to fill the space outside of the gradient region.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient2.png"/>
The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface specifies one and only one stop in a gradient.

The calculations used to render a gradient are described in the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.

The code example that follows illustrates how this method is used to create a new  interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMGradientStop    *newInterface;
// The following values are defined outside of 
// this example.
//  XPS_COLOR                    color;
//  IXpsOMColorProfileResource    *colorProfile;
//  FLOAT                        offset;

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
    hr = xpsFactory-&gt;CreateGradientStop (
        &amp;color,
        colorProfile,
        offset,
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




<a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a>



<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a>
 

 

