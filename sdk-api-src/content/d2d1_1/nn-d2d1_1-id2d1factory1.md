---
UID: NN:d2d1_1.ID2D1Factory1
title: ID2D1Factory1
author: windows-sdk-content
description: Creates Direct2D resources.
old-location: direct2d\id2d1factory1.htm
tech.root: Direct2D
ms.assetid: 8221c3b4-e331-403c-9406-ee8d3e103825
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1Factory1, ID2D1Factory1 interface [Direct2D], ID2D1Factory1 interface [Direct2D],described, d2d1_1/ID2D1Factory1, direct2d.id2d1factory1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID2D1Factory1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1 interface


## -description


Creates Direct2D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Factory1</b> interface inherits from <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>. <b>ID2D1Factory1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Factory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d16569c1-e366-45fe-9079-ed9eb894547b">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4FB5484A-D872-4610-AC77-D4CE3DB8EB70">CreateDrawingStateBlock</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new drawing state block, this can be used in subsequent
    SaveDrawingState and RestoreDrawingState operations on the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/580DF262-2A86-4C21-8DFA-A804CE0A79CC">CreateGdiMetafile</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a> object that you can use to replay metafile content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/182e7dbc-ab49-427f-8801-d94e4ed9a308">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/21f0a4a3-3c6c-434d-8cfc-767c7654849e">ID2D1PathGeometry1</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FFC85600-A352-4348-BFAA-CBCAF34A692C">CreateStrokeStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates a <a href="https://msdn.microsoft.com/7afaa6f8-8e25-42ec-9afb-a5342bba11d0">ID2D1StrokeStyle1</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e8a2f03-f297-4d5a-8461-4ed7cd1bf02f">GetEffectProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of an effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3363411-908f-4b02-b77e-ca563094f9a5">GetRegisteredEffects</a>
</td>
<td align="left" width="63%">
Returns the class IDs of the currently registered effects and global effects on this factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E22F04F3-A67E-4F93-B936-5AE5CDFF75EF">RegisterEffectFromStream</a>
</td>
<td align="left" width="63%">
Registers an effect within the factory instance with the property XML specified as a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9988aad6-0487-4f48-a05c-1dfb944f6ce7">RegisterEffectFromString</a>
</td>
<td align="left" width="63%">
Registers an effect within the factory instance with the property XML specified as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f383406-5d83-4ccc-9082-526b9e9fa80b">UnregisterEffect</a>
</td>
<td align="left" width="63%">
Unregisters an  effect within the factory instance that corresponds to the <i>classId</i> provided. 

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1Factory1</b> interface is used to create devices, register and unregister effects, and enumerate effects properties. Effects are registered and unregistered globally. The registration APIs are placed on this interface for convenience.
        




## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>



<a href="https://msdn.microsoft.com/FDD770D4-817F-44D9-86C4-15DD04D214AE">Multithreaded Direct2D Apps</a>
 

 

