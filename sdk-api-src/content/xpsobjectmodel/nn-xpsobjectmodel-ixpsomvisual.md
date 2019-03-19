---
UID: NN:xpsobjectmodel.IXpsOMVisual
title: IXpsOMVisual (xpsobjectmodel.h)
author: windows-sdk-content
description: The base interface for path, canvas, and glyph interfaces.
old-location: xps\ixpsomvisual.htm
tech.root: printdocs
ms.assetid: f2ec412c-aece-4b20-a721-e6c17615e56b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMVisual, IXpsOMVisual interface [XPS Documents and Packaging], IXpsOMVisual interface [XPS Documents and Packaging],described, xps.ixpsomvisual, xpsobjectmodel/IXpsOMVisual
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
 - IXpsOMVisual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisual interface


## -description


The  base interface for path, canvas, and glyph interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMVisual</b> interface inherits from <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>. <b>IXpsOMVisual</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMVisual</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f56fa077-749c-422b-b82d-161f9e5d4766">GetClipGeometry</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the resolved geometry of the visual's clipping region.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19efe0d7-6b11-41bc-80e7-e43e64d977b4">GetClipGeometryLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the local, unshared geometry of the visual's clipping region.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa101ac6-65e8-4f6b-a6fa-59f3a003ffc5">GetClipGeometryLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key for the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface in a resource dictionary that contains the visual's clipping region.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/297ddac1-8383-423a-8e47-7b4466e7e5d1">GetHyperlinkNavigateUri</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a> interface  to which this visual object links.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd6047a6-d6ba-4c62-8f4c-0348e3281d75">GetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the visual is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22cddce5-f881-4585-9ab8-d8cdce06511f">GetLanguage</a>
</td>
<td align="left" width="63%">
Gets the <b>Language</b> property of the visual and of its contents.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a8b592e-c80e-4a0f-b9a4-8c362da43ced">GetName</a>
</td>
<td align="left" width="63%">
Gets the <b>Name</b> property of the visual.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c513ea28-937a-4594-9a50-0c7999f435ce">GetOpacity</a>
</td>
<td align="left" width="63%">
Gets the opacity value of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df5b770e-cc66-45ee-b865-2959255920bf">GetOpacityMaskBrush</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface of the visual's opacity mask brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/654dc003-25a6-4186-9c3b-7fe6f82b5481">GetOpacityMaskBrushLocal</a>
</td>
<td align="left" width="63%">
Gets the local, unshared opacity mask brush for the visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84d4aae9-e3e3-4c82-8877-b8206d3678f0">GetOpacityMaskBrushLookup</a>
</td>
<td align="left" width="63%">
Gets the name of the lookup key of the  shared opacity mask brush in a resource dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/966916c9-8b63-468b-80fb-0c4863ff893a">GetTransform</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the visual's resolved matrix transform.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7152ba0-2b65-4c66-b99b-7450a8cdb6fd">GetTransformLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the local, unshared, resolved matrix transform for the visual.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83d30b9c-4d3d-4fca-8dea-121074642b39">GetTransformLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key name of the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface in a resource dictionary that contains the resolved matrix transform for the visual.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b703866-9dc0-4327-9988-908f17bd4b21">SetClipGeometryLocal</a>
</td>
<td align="left" width="63%">
Sets the local, unshared clipping region for the visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f79f1ce-e761-44f7-970c-393c83f8f2fd">SetClipGeometryLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared clip geometry in a resource dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6909d287-67c8-4f01-8523-6011932d1d34">SetHyperlinkNavigateUri</a>
</td>
<td align="left" width="63%">
Sets the destination URI of the visual's hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/855a3993-b308-4dc0-a2f6-8ac6bdc495ce">SetIsHyperlinkTarget</a>
</td>
<td align="left" width="63%">
Specifies whether the visual is the target of a hyperlink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19a7c10d-ceea-4303-a655-a3cb8b910377">SetLanguage</a>
</td>
<td align="left" width="63%">
Sets the <b>Language</b> property of the visual.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bf30b4c-bddf-4ca8-91c6-af739125829c">SetName</a>
</td>
<td align="left" width="63%">
Sets the <b>Name</b>  property of the visual.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a29aee3-f11b-41e7-a871-3be3d5994409">SetOpacity</a>
</td>
<td align="left" width="63%">
Sets the opacity value of the visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b84156-b7ad-4dac-97d9-60aaedcee210">SetOpacityMaskBrushLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface pointer as the local, unshared opacity mask brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared opacity mask brush in a resource dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac087cb0-dd3c-4f4b-a6e0-6f0f0a219d8a">SetTransformLocal</a>
</td>
<td align="left" width="63%">
Sets the local, unshared matrix transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9066cf8-37b5-4c30-ae41-f92a61aa552c">SetTransformLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared matrix transform in a resource dictionary.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/6d2cda65-c719-46f2-97c9-8aee7b5f84b9">IXpsOMGlyphs</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

