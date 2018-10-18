---
UID: NN:d2d1svg.ID2D1SvgPathData
title: ID2D1SvgPathData
author: windows-sdk-content
description: Interface describing SVG path data. Path data can be set as the 'd' attribute on a 'path' element.
old-location: direct2d\id2d1svgpathdata.htm
tech.root: direct2d
ms.assetid: 14879B17-0CAA-42E7-8643-7D385EABFD37
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1SvgPathData, ID2D1SvgPathData interface [Direct2D], ID2D1SvgPathData interface [Direct2D],described, d2d1svg/ID2D1SvgPathData, direct2d.id2d1svgpathdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPathData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPathData interface


## -description


Interface describing SVG path data. Path data can be set as the 'd' attribute on a 'path' element.

The path data set is factored into two arrays. The segment data array stores all
        numbers and the commands array stores the set of commands. Unlike the string
        data set in the d attribute, each command in this representation uses a fixed
        number of elements in the segment data array. Therefore, the path 'M 0,0 100,0
        0,100 Z' is represented as: 'M0,0 L100,0 L0,100 Z'. This is split into two
        arrays, with the segment data containing '0,0 100,0 0,100', and the commands
        containing 'M L L Z'.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPathData</b> interface inherits from <a href="https://msdn.microsoft.com/7B11D05C-6CD5-4609-B76A-719B92437314">ID2D1SvgAttribute</a>. <b>ID2D1SvgPathData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgPathData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BDF23A0F-EC4B-49AE-8822-9326DA2D885D">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates a path geometry object representing the path data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D72199E5-11E5-413E-88F0-85EF17585587">GetCommands</a>
</td>
<td align="left" width="63%">
Gets commands from the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FF5AC30D-6EEF-4963-BC1C-979F8747DABA">GetCommandsCount</a>
</td>
<td align="left" width="63%">
Gets the size of the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D935BCEB-D7B8-4245-AD1C-25BAE63F8944">GetSegmentData</a>
</td>
<td align="left" width="63%">
Gets data from the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93D41E54-8D09-46E9-A83F-87C84F26B9C4">GetSegmentDataCount</a>
</td>
<td align="left" width="63%">
Gets the size of the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1DB006D-9986-482A-A9F0-9D7C22ABC604">RemoveCommandsAtEnd</a>
</td>
<td align="left" width="63%">
Removes commands from the end of the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/549531A1-099D-477E-8D77-CF90BD75FAB8">RemoveSegmentDataAtEnd</a>
</td>
<td align="left" width="63%">
Removes data from the end of the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6A6BC06-01C4-47D0-BC3C-7E0CE1A926F4">UpdateCommands</a>
</td>
<td align="left" width="63%">
Updates the commands array. Existing commands not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3B87B002-7F1C-4531-B584-C0CFC8E46256">UpdateSegmentData</a>
</td>
<td align="left" width="63%">
Updates the segment data array. Existing segment data not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new segment data.

</td>
</tr>
</table> 

