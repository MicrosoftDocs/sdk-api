---
UID: NN:xpsobjectmodel.IXpsOMPath
title: IXpsOMPath (xpsobjectmodel.h)
description: Describes a non-text visual item.helpviewer_keywords: ["IXpsOMPath","IXpsOMPath interface [XPS Documents and Packaging]","IXpsOMPath interface [XPS Documents and Packaging]","described","xps.ixpsompath","xpsobjectmodel/IXpsOMPath"]
old-location: xps\ixpsompath.htm
tech.root: printdocs
ms.assetid: 93257a77-3fef-400e-bfe1-06e760ba4b93
ms.date: 12/05/2018
ms.keywords: IXpsOMPath, IXpsOMPath interface [XPS Documents and Packaging], IXpsOMPath interface [XPS Documents and Packaging],described, xps.ixpsompath, xpsobjectmodel/IXpsOMPath
f1_keywords:
- xpsobjectmodel/IXpsOMPath
dev_langs:
- c++
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
- IXpsOMPath
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPath interface


## -description


Describes a non-text visual item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPath</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>. <b>IXpsOMPath</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPath</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getaccessibilitylongdescription">GetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Gets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getaccessibilityshortdescription">GetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Gets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrush">GetFillBrush</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the fill brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrushlocal">GetFillBrushLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the local, unshared <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the fill brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getfillbrushlookup">GetFillBrushLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of the brush that is stored in a resource dictionary and used as the fill brush for the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometry">GetGeometry</a>
</td>
<td align="left" width="63%">
Gets a pointer to the path's <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface, which describes the  resolved fill area for this path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometrylocal">GetGeometryLocal</a>
</td>
<td align="left" width="63%">
Gets the local, unshared geometry of the  resolved fill area for this path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometrylookup">GetGeometryLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of a shared geometry object that is stored in a resource dictionary and that describes the  resolved fill area for this path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getsnapstopixels">GetSnapsToPixels</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the path is to  be snapped to device pixels when the path is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrush">GetStrokeBrush</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the stroke brush that has been set for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrushlocal">GetStrokeBrushLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the local, unshared <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface that contains the stroke brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokebrushlookup">GetStrokeBrushLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of the brush  that is stored in a resource dictionary and is to be used as the stroke brush for the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashcap">GetStrokeDashCap</a>
</td>
<td align="left" width="63%">
Gets the style of the end cap to be used on the stroke dash.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes">GetStrokeDashes</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a> interface that contains the <a href="https://docs.microsoft.com/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structures that  define the dash pattern of the stroke.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashoffset">GetStrokeDashOffset</a>
</td>
<td align="left" width="63%">
Gets the offset from the origin of the stroke to the starting point of the dash array pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokeendlinecap">GetStrokeEndLineCap</a>
</td>
<td align="left" width="63%">
Gets the style of the stroke line's  end cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokelinejoin">GetStrokeLineJoin</a>
</td>
<td align="left" width="63%">
Gets the style for joining stroke lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokemiterlimit">GetStrokeMiterLimit</a>
</td>
<td align="left" width="63%">
Gets the miter limit value that is  set for the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokestartlinecap">GetStrokeStartLineCap</a>
</td>
<td align="left" width="63%">
Gets the style of the  line cap at the start of the stroke line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokethickness">GetStrokeThickness</a>
</td>
<td align="left" width="63%">
Gets the stroke thickness.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription">SetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Sets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription">SetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Sets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlocal">SetFillBrushLocal</a>
</td>
<td align="left" width="63%">
Sets the pointer to the local, unshared <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface to be used as the fill brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setfillbrushlookup">SetFillBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>
</td>
<td align="left" width="63%">
Sets the pointer to the local, unshared <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface that contains the  geometry of the resolved fill area to be set for this path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylookup">SetGeometryLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared geometry in a resource dictionary. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setsnapstopixels">SetSnapsToPixels</a>
</td>
<td align="left" width="63%">
Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal">SetStrokeBrushLocal</a>
</td>
<td align="left" width="63%">
Sets a pointer to a local, unshared <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a> interface to be used as a stroke brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared brush to be used as the stroke brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap">SetStrokeDashCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke's dash cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset">SetStrokeDashOffset</a>
</td>
<td align="left" width="63%">
Sets the offset from the origin of the stroke to the starting point of the dash array pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap">SetStrokeEndLineCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke line's end cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin">SetStrokeLineJoin</a>
</td>
<td align="left" width="63%">
Sets the  style for joining stroke lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit">SetStrokeMiterLimit</a>
</td>
<td align="left" width="63%">
Sets the miter limit of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap">SetStrokeStartLineCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke's line cap at the  start of the stroke line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness">SetStrokeThickness</a>
</td>
<td align="left" width="63%">
Sets the stroke thickness.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.


```cpp

IXpsOMPath    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreatePath (&newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpath">IXpsOMObjectFactory::CreatePath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://www.microsoft.com/download/details.aspx?id=11816">XML Paper Specification</a>
 

 

