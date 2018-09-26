---
UID: NE:d2d1.D2D1_COMBINE_MODE
title: D2D1_COMBINE_MODE
author: windows-sdk-content
description: Specifies the different methods by which two geometries can be combined.
old-location: direct2d\D2D1_COMBINE_MODE.htm
tech.root: direct2d
ms.assetid: 7526379a-5f57-4a9f-b85d-415f131528e2
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: D2D1_COMBINE_MODE, D2D1_COMBINE_MODE enumeration [Direct2D], D2D1_COMBINE_MODE_EXCLUDE, D2D1_COMBINE_MODE_INTERSECT, D2D1_COMBINE_MODE_UNION, D2D1_COMBINE_MODE_XOR, d2d1/D2D1_COMBINE_MODE, d2d1/D2D1_COMBINE_MODE_EXCLUDE, d2d1/D2D1_COMBINE_MODE_INTERSECT, d2d1/D2D1_COMBINE_MODE_UNION, d2d1/D2D1_COMBINE_MODE_XOR, direct2d.D2D1_COMBINE_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_COMBINE_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_COMBINE_MODE
req.redist: 
---

# D2D1_COMBINE_MODE enumeration


## -description


Specifies the different methods by which two geometries can be combined.


## -enum-fields




### -field D2D1_COMBINE_MODE_UNION

The two regions are combined by taking the union of both. Given two geometries, <i>A</i> and <i>B</i>, the resulting geometry is geometry <i>A</i> + geometry <i>B</i>.


### -field D2D1_COMBINE_MODE_INTERSECT

The two regions are combined by taking their intersection. The new area consists of the overlapping region between the two geometries. 


### -field D2D1_COMBINE_MODE_XOR

The two regions are combined by taking the area that exists in the first region but not the second and the area that exists in the second region but not the first. Given two geometries, <i>A</i> and <i>B</i>, the new region consists of (<i>A</i>-<i>B</i>) + (<i>B</i>-<i>A</i>). 


### -field D2D1_COMBINE_MODE_EXCLUDE

The second region is excluded from the first. Given two geometries, <i>A</i> and <i>B</i>, the area of geometry <i>B</i> is removed from the area of geometry <i>A</i>, producing a region that is <i>A</i>-<i>B</i>.


### -field D2D1_COMBINE_MODE_FORCE_DWORD




## -remarks



The following illustration shows the different geometry combine modes.


<img alt="Illustration of two geometries and the resulting shapes after various geometry combine modes" src="./images/geometry_combine_modes.png"/>

#### Examples

The following code uses each of the different combine modes to combine two <a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">ID2D1EllipseGeometry</a> objects. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory-&gt;CreateEllipseGeometry(
        circle1,
        &amp;m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory-&gt;CreateEllipseGeometry(circle2, &amp;m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory-&gt;CreatePathGeometry(&amp;m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion-&gt;Open(&amp;pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1-&gt;CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink-&gt;Close();
            }

            SafeRelease(&amp;pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory-&gt;CreatePathGeometry(&amp;m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect-&gt;Open(&amp;pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1-&gt;CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink-&gt;Close();
            }

            SafeRelease(&amp;pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory-&gt;CreatePathGeometry(&amp;m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR-&gt;Open(&amp;pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1-&gt;CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink-&gt;Close();
            }

            SafeRelease(&amp;pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory-&gt;CreatePathGeometry(&amp;m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude-&gt;Open(&amp;pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1-&gt;CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink-&gt;Close();
            }

            SafeRelease(&amp;pGeometrySink);
        }
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


