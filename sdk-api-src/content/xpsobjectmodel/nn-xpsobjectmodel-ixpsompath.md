---
UID: NN:xpsobjectmodel.IXpsOMPath
title: IXpsOMPath
author: windows-sdk-content
description: Describes a non-text visual item.
old-location: xps\ixpsompath.htm
tech.root: printdocs
ms.assetid: 93257a77-3fef-400e-bfe1-06e760ba4b93
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMPath, IXpsOMPath interface [XPS Documents and Packaging], IXpsOMPath interface [XPS Documents and Packaging],described, xps.ixpsompath, xpsobjectmodel/IXpsOMPath
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath interface


## -description


Describes a non-text visual item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPath</b> interface inherits from <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>. <b>IXpsOMPath</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4602f9fe-6001-4a5a-8870-f2a6e97ccc55">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ec32c0c-c6d3-4de0-a896-bf191805e799">GetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Gets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0124d37a-74c1-4f8b-9d91-c12e92cd5e8c">GetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Gets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc121659-c04f-433a-aaf7-ab7ecd1fd763">GetFillBrush</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that contains the fill brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c5a7150-19d6-40aa-871b-5600c0b0a947">GetFillBrushLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that contains the fill brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89433357-fa39-41e9-bd21-ff3c076261db">GetFillBrushLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of the brush that is stored in a resource dictionary and used as the fill brush for the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4a99bf6-09d8-426a-8878-1126578c4518">GetGeometry</a>
</td>
<td align="left" width="63%">
Gets a pointer to the path's <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface, which describes the  resolved fill area for this path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8902191-7646-4c97-843f-9467ed12f621">GetGeometryLocal</a>
</td>
<td align="left" width="63%">
Gets the local, unshared geometry of the  resolved fill area for this path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f40b6ed0-6e75-4f0a-abcc-f13d961df678">GetGeometryLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of a shared geometry object that is stored in a resource dictionary and that describes the  resolved fill area for this path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0a4a8b5-f7cf-4cbe-9221-41cde4f63557">GetSnapsToPixels</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the path is to  be snapped to device pixels when the path is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf786b0-5603-4735-8770-4c5e17a67253">GetStrokeBrush</a>
</td>
<td align="left" width="63%">
Gets a pointer to the resolved <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that contains the stroke brush that has been set for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf816750-8381-4c04-af20-e5ce3f8ad63c">GetStrokeBrushLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface that contains the stroke brush for the path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af70b6a3-203a-4189-b44d-763539e0302a">GetStrokeBrushLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key of the brush  that is stored in a resource dictionary and is to be used as the stroke brush for the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afd33b39-3aeb-41eb-8747-7d1cff0aaa38">GetStrokeDashCap</a>
</td>
<td align="left" width="63%">
Gets the style of the end cap to be used on the stroke dash.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60c76c8f-1434-4347-9639-a886d6ae133c">GetStrokeDashes</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/02a152a1-e117-42fb-8428-a2b28e6540a9">IXpsOMDashCollection</a> interface that contains the <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structures that  define the dash pattern of the stroke.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/173e820f-e926-44cc-a6ba-54edde770f73">GetStrokeDashOffset</a>
</td>
<td align="left" width="63%">
Gets the offset from the origin of the stroke to the starting point of the dash array pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b4f6e7-3a76-48d3-a180-2bb3a532fc67">GetStrokeEndLineCap</a>
</td>
<td align="left" width="63%">
Gets the style of the stroke line's  end cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e460f22-7997-419a-86b7-a0beace1bc27">GetStrokeLineJoin</a>
</td>
<td align="left" width="63%">
Gets the style for joining stroke lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4271c7ff-636c-4ab0-b83f-90c769baf74c">GetStrokeMiterLimit</a>
</td>
<td align="left" width="63%">
Gets the miter limit value that is  set for the stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66286aca-3b94-4ded-9180-1e07599986db">GetStrokeStartLineCap</a>
</td>
<td align="left" width="63%">
Gets the style of the  line cap at the start of the stroke line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c1d8179-99e6-4335-8777-56b6873f746b">GetStrokeThickness</a>
</td>
<td align="left" width="63%">
Gets the stroke thickness.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9727cbea-55f7-48ad-8205-d68d0c906250">SetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Sets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e078817-be7c-493c-9b46-9c9f4068745c">SetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Sets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>
</td>
<td align="left" width="63%">
Sets the pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as the fill brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32657c0d-3be5-466c-98a7-6bbd46f710d1">SetGeometryLocal</a>
</td>
<td align="left" width="63%">
Sets the pointer to the local, unshared <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the  geometry of the resolved fill area to be set for this path.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a60bf60-e69b-4a8a-94e9-5d304aa25dd5">SetGeometryLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared geometry in a resource dictionary. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b063829-3941-42be-bbe2-49b5a71b695a">SetSnapsToPixels</a>
</td>
<td align="left" width="63%">
Sets a Boolean value that indicates whether the path will be snapped to device pixels when that path is being rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/551bc4e2-2bf3-455b-a7f1-35b3b66697c0">SetStrokeBrushLocal</a>
</td>
<td align="left" width="63%">
Sets a pointer to a local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as a stroke brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared brush to be used as the stroke brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/949f366b-1161-4db8-b9b9-d95b422b8931">SetStrokeDashCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke's dash cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6d222e4-9480-4dc7-9963-7dd637892281">SetStrokeDashOffset</a>
</td>
<td align="left" width="63%">
Sets the offset from the origin of the stroke to the starting point of the dash array pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f223503c-4934-4b3d-b489-c8f6488b05d0">SetStrokeEndLineCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke line's end cap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd650051-ee26-4a8a-b344-2fe84fb2c2a5">SetStrokeLineJoin</a>
</td>
<td align="left" width="63%">
Sets the  style for joining stroke lines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e33f9f3-119a-4635-b44c-fa002a59fa20">SetStrokeMiterLimit</a>
</td>
<td align="left" width="63%">
Sets the miter limit of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b465775-6eda-49cb-aa9a-091e4d815da3">SetStrokeStartLineCap</a>
</td>
<td align="left" width="63%">
Sets the style of the stroke's line cap at the  start of the stroke line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e16774e2-9c70-46b6-a894-e289cdee47b3">SetStrokeThickness</a>
</td>
<td align="left" width="63%">
Sets the stroke thickness.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMPath    *newInterface;

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
    hr = xpsFactory-&gt;CreatePath (&amp;newInterface);

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




<a href="https://msdn.microsoft.com/aa5dcddd-9ca7-4b8f-9f4f-aa0f851e8697">IXpsOMObjectFactory::CreatePath</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

