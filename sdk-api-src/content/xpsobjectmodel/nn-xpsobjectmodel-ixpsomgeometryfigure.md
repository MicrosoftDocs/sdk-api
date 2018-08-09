---
UID: NN:xpsobjectmodel.IXpsOMGeometryFigure
title: IXpsOMGeometryFigure
author: windows-sdk-content
description: Describes one portion of the path or clipping region that is specified by an IXpsOMGeometry interface.
old-location: xps\ixpsomgeometryfigure.htm
old-project: printdocs
ms.assetid: e76a14ce-cfc3-4a50-855e-f5779b9fc261
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMGeometryFigure, IXpsOMGeometryFigure interface [XPS Documents and Packaging], IXpsOMGeometryFigure interface [XPS Documents and Packaging],described, xps.ixpsomgeometryfigure, xpsobjectmodel/IXpsOMGeometryFigure
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMGeometryFigure
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure interface


## -description


Describes one portion of the path or clipping region that is specified by an <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMGeometryFigure</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMGeometryFigure</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMGeometryFigure</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7ab38b8-b378-4804-9d07-4644161b1450">GetIsClosed</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the figure is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22da5239-c79f-4306-ad60-9b3e5bcae988">GetIsFilled</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the figure is filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/520e52ff-fb65-430f-972c-40ca2ab959b2">GetOwner</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the geometry figure.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b302c0-31e3-460b-9771-3f293c94447a">GetSegmentCount</a>
</td>
<td align="left" width="63%">
Gets the number of segments in the figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e6be6f-3a9d-4d39-875f-cd23bc82e74b">GetSegmentData</a>
</td>
<td align="left" width="63%">
Gets the segment data points for the geometry figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42b68a76-e7fe-49d2-9190-4a4d5e763052">GetSegmentDataCount</a>
</td>
<td align="left" width="63%">
Gets the number of segment data points in the figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/497701aa-8738-43d1-830f-7a6c00cfa2cc">GetSegmentStrokePattern</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/e824884e-ffad-4c44-9df8-e9c21e1f3758">XPS_SEGMENT_STROKE_PATTERN</a> value that indicates whether the segments in the figure are stroked.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97832bcb-c193-48e2-84f5-21b9c5a55cc9">GetSegmentStrokes</a>
</td>
<td align="left" width="63%">
Gets stroke definitions for the figure's segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a440c227-33c9-42f9-8f4a-4cbe6281f9ad">GetSegmentTypes</a>
</td>
<td align="left" width="63%">
Gets the types of segments in the figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dbd829e-eaae-42f4-ae39-9ec35cbd3102">GetStartPoint</a>
</td>
<td align="left" width="63%">
Gets the starting point of the figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c839d2d-8887-464e-8052-b9092a41eeb3">SetIsClosed</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the figure is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18054987-35a9-4049-ba0f-1425e2e54ed3">SetIsFilled</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the figure is filled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e2a1a80-1eda-458f-b711-de56df7a98ac">SetSegments</a>
</td>
<td align="left" width="63%">
Sets the segment information and data points for the segments in the figure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9885c3d-06a0-4d25-81fc-cf0ef466a797">SetStartPoint</a>
</td>
<td align="left" width="63%">
Sets the starting point of the figure.

</td>
</tr>
</table> 


## -remarks



The <b>IXpsOMGeometryFigure</b> corresponds to the <b>PathFigure</b> element in XPS markup.

The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreateGeometryFigure (&amp;startPoint, &amp;newInterface);
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




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/d9138dbc-5a9e-4653-bab2-71f6d716eba6">IXpsOMObjectFactory::CreateGeometryFigure</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/e824884e-ffad-4c44-9df8-e9c21e1f3758">XPS_SEGMENT_STROKE_PATTERN</a>
 

 

