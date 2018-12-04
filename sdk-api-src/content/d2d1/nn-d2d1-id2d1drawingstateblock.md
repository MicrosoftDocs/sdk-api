---
UID: NN:d2d1.ID2D1DrawingStateBlock
title: ID2D1DrawingStateBlock
author: windows-sdk-content
description: Represents the drawing state of a render target:\_the antialiasing mode, transform, tags, and text-rendering options.
old-location: direct2d\ID2D1DrawingStateBlock.htm
tech.root: direct2d
ms.assetid: 9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID2D1DrawingStateBlock, ID2D1DrawingStateBlock interface [Direct2D], ID2D1DrawingStateBlock interface [Direct2D],described, d2d1/ID2D1DrawingStateBlock, direct2d.ID2D1DrawingStateBlock
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1DrawingStateBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawingStateBlock interface


## -description


Represents the drawing state of a render target: the antialiasing mode, transform, tags, and text-rendering options.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DrawingStateBlock</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1DrawingStateBlock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DrawingStateBlock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41c80a2d-0a20-4515-88b0-1878ba6aa945">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the antialiasing mode, transform, and tags portion of the drawing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86822497-e256-445b-8da9-9ead229f89ee">GetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Retrieves the text-rendering configuration of the drawing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e967eb49-0cfd-4e8b-955c-83a6b3a1859b">SetDescription</a>
</td>
<td align="left" width="63%">Overloaded. Specifies the antialiasing mode, transform, and tags portion of the drawing state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/449bd558-a3f1-4168-a803-d2f00b2250d2">SetTextRenderingParams</a>
</td>
<td align="left" width="63%">
Specifies the text-rendering configuration of the drawing state.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1DrawingStateBlock_Objects"></a><a id="creating_id2d1drawingstateblock_objects"></a><a id="CREATING_ID2D1DRAWINGSTATEBLOCK_OBJECTS"></a>Creating ID2D1DrawingStateBlock Objects</h3>
To create an <b>ID2D1DrawingStateBlock</b>, use the <a href="https://msdn.microsoft.com/c2b5875f-9f14-4752-a426-2745fdaa543a">ID2D1Factory::CreateDrawingStateBlock</a> method.

A drawing state block is a device-independent resource; you can create it once and retain it for the life of your application. For more information about resources, see the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

