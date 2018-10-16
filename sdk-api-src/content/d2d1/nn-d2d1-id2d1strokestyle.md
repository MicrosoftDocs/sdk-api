---
UID: NN:d2d1.ID2D1StrokeStyle
title: ID2D1StrokeStyle
author: windows-sdk-content
description: Describes the caps, miter limit, line join, and dash information for a stroke.
old-location: direct2d\ID2D1StrokeStyle.htm
tech.root: direct2d
ms.assetid: 2cdf66dc-f34f-4132-8c06-7464648d3cef
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ID2D1StrokeStyle, ID2D1StrokeStyle interface [Direct2D], ID2D1StrokeStyle interface [Direct2D],described, d2d1/ID2D1StrokeStyle, direct2d.ID2D1StrokeStyle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1StrokeStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1StrokeStyle interface


## -description


Describes the caps, miter limit, line join, and dash information for a stroke.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1StrokeStyle</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1StrokeStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1StrokeStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e5d760-dee0-4360-be47-6db9870d51f1">GetDashCap</a>
</td>
<td align="left" width="63%">
Gets a value that specifies how the ends of each dash are drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5add3b9-e052-4727-b14f-543fa452ad6d">GetDashes</a>
</td>
<td align="left" width="63%">
Copies the dash pattern to the specified array. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bd1df70-17db-4f0f-b7a4-b26601b23c44">GetDashesCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the dashes array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db540976-95a7-47c9-aeec-d5f874d22764">GetDashOffset</a>
</td>
<td align="left" width="63%">
Retrieves a value that specifies how far in the dash sequence the stroke will start. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15d61f2c-9348-47af-a9cf-4706ab0033b7">GetDashStyle</a>
</td>
<td align="left" width="63%">
Gets a value that describes the stroke's dash pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06cf4629-9fa8-471a-9f92-94bdfb18c2d1">GetEndCap</a>
</td>
<td align="left" width="63%">
Retrieves the type of shape used at the end of a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408e473d-c143-490e-98c3-2da312aa0c94">GetLineJoin</a>
</td>
<td align="left" width="63%">
Retrieves the type of joint used at the vertices of a shape's outline. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29748b05-830b-48ae-9303-a5f7852792e7">GetMiterLimit</a>
</td>
<td align="left" width="63%">
Retrieves the limit on the ratio of the miter length to half the stroke's thickness.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8df80ac7-8dad-418f-bff5-14c39ad38fac">GetStartCap</a>
</td>
<td align="left" width="63%">
Retrieves the type of shape used at the beginning of a stroke.  

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1StrokeStyle_Objects"></a><a id="creating_id2d1strokestyle_objects"></a><a id="CREATING_ID2D1STROKESTYLE_OBJECTS"></a>Creating ID2D1StrokeStyle Objects</h3>
To create a stroke style, use the <a href="https://msdn.microsoft.com/cc7bd68b-a6eb-4d05-b331-032ce80f375c">ID2D1Factory::CreateStrokeStyle</a> method.

A stroke style is a device-indenpendent resource; you can create it once then retain it for the life of your application. For more information about resources, see the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.


#### Examples

The following example creates a stroke that uses a custom dash pattern.
        
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory-&gt;CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &amp;m_pStrokeStyleCustomOffsetZero
        );
}
</pre>
</td>
</tr>
</table></span></div>
The next example uses the stroke style when drawing a line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>m_pRenderTarget-&gt;DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cc7bd68b-a6eb-4d05-b331-032ce80f375c">ID2D1Factory::CreateStrokeStyle</a>



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

