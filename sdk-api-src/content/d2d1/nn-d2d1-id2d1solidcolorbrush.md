---
UID: NN:d2d1.ID2D1SolidColorBrush
title: ID2D1SolidColorBrush
author: windows-sdk-content
description: Paints an area with a solid color.
old-location: direct2d\ID2D1SolidColorBrush.htm
tech.root: Direct2D
ms.assetid: a15c2696-3122-461e-806e-2195a50a3e92
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1SolidColorBrush, ID2D1SolidColorBrush interface [Direct2D], ID2D1SolidColorBrush interface [Direct2D],described, d2d1/ID2D1SolidColorBrush, direct2d.ID2D1SolidColorBrush
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
 - ID2D1SolidColorBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SolidColorBrush interface


## -description


Paints an area with a solid color.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SolidColorBrush</b> interface inherits from <a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>. <b>ID2D1SolidColorBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SolidColorBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25eac791-9402-4202-8e00-936d355d8d2b">GetColor</a>
</td>
<td align="left" width="63%">
Retrieves the color of the solid color brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2900bf72-9641-419c-b0d7-334f14f8a474">SetColor</a>
</td>
<td align="left" width="63%">Overloaded. Specifies the color of this solid color brush. 

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1SolidColorBrush_Objects"></a><a id="creating_id2d1solidcolorbrush_objects"></a><a id="CREATING_ID2D1SOLIDCOLORBRUSH_OBJECTS"></a>Creating ID2D1SolidColorBrush Objects</h3>
To create a solid color brush, use the <a href="https://msdn.microsoft.com/en-us/library/Dd742843(v=VS.85).aspx">ID2D1RenderTarget::CreateSolidColorBrush</a> method of the render target  on which the brush will be used. The brush can only be used with the render target that created it or with  the compatible targets for that render target.

A solid color brush is a device-dependent resource. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/en-us/library/Dd742843(v=VS.85).aspx">CreateSolidColorBrush</a> method of a render target (<i>m_pRenderTarget</i>) to create two brushes. The example uses a predefined color (black) to specify the color of the first brush. It uses a hexadecimal color value (yellow) to specify the color of the second brush.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
</pre>
</td>
</tr>
</table></span></div>


The next code example calls the <a href="https://msdn.microsoft.com/b5d7ca28-0751-4799-8480-f221fd5fe276">FillRectangle</a> method to paint the interior of a rectangle with the yellow green brush and the <a href="https://msdn.microsoft.com/bc176c12-db06-4f1e-b668-4441723a916a">DrawRectangle</a> method to paint the outline of the rectangle with the black brush:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
</pre>
</td>
</tr>
</table></span></div>


These examples produce the output shown in the following illustration.

<img alt="Illustration of a rectangle filled with a solid, yellow-green color" src="./images/brushes_ovw_solidcolor.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/36f5cf3e-00a4-45d2-816c-85c18eb948f4">ColorF</a>



<a href="https://msdn.microsoft.com/70700b82-2294-46be-b1c0-fc89def441e2">How to Create a Solid Color Brush</a>



<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

