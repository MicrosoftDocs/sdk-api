---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D2D1_DASH_STYLE enumeration


## -description


Describes the sequence of dashes and gaps in a stroke.


## -enum-fields




### -field D2D1_DASH_STYLE_SOLID

A solid line with no breaks.


### -field D2D1_DASH_STYLE_DASH

A dash followed by a gap of equal length. The dash and the gap are each twice as long as the stroke thickness.

The equivalent dash  array for  <b>D2D1_DASH_STYLE_DASH</b> is {2, 2}.


### -field D2D1_DASH_STYLE_DOT

A dot followed by a longer gap.

The equivalent dash  array for  <b>D2D1_DASH_STYLE_DOT</b> is {0, 2}.


### -field D2D1_DASH_STYLE_DASH_DOT

A dash, followed by a gap, followed by a dot, followed by another gap.

The equivalent dash array for  <b>D2D1_DASH_STYLE_DASH_DOT</b> is {2, 2, 0, 2}.


### -field D2D1_DASH_STYLE_DASH_DOT_DOT

A dash, followed by a gap, followed by a dot, followed by another gap, followed by another dot, followed by another gap.

The equivalent dash array for  <b>D2D1_DASH_STYLE_DASH_DOT_DOT</b> is {2, 2, 0, 2, 0, 2}.


### -field D2D1_DASH_STYLE_CUSTOM

The dash pattern is specified by an array of floating-point values.


### -field D2D1_DASH_STYLE_FORCE_DWORD




## -remarks



The following illustration shows several available dash styles. 
      

<img alt="Illustration of available dash styles" src="images/StrokeStyle_DashStyle.png"/>

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


