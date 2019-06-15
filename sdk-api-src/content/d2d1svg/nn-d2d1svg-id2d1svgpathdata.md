---
UID: NN:d2d1svg.ID2D1SvgPathData
title: ID2D1SvgPathData (d2d1svg.h)
author: windows-sdk-content
description: Interface describing SVG path data. Path data can be set as the 'd' attribute on a 'path' element.
old-location: direct2d\id2d1svgpathdata.htm
tech.root: Direct2D
ms.assetid: 14879B17-0CAA-42E7-8643-7D385EABFD37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPathData, ID2D1SvgPathData interface [Direct2D], ID2D1SvgPathData interface [Direct2D],described, d2d1svg/ID2D1SvgPathData, direct2d.id2d1svgpathdata
ms.topic: interface
f1_keywords: ["d2d1svg/ID2D1SvgPathData"]
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
ms.custom: 19H1
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgPathData</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgattribute">ID2D1SvgAttribute</a>. <b>ID2D1SvgPathData</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-createpathgeometry">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates a path geometry object representing the path data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-getcommands">GetCommands</a>
</td>
<td align="left" width="63%">
Gets commands from the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-getcommandscount">GetCommandsCount</a>
</td>
<td align="left" width="63%">
Gets the size of the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-getsegmentdata">GetSegmentData</a>
</td>
<td align="left" width="63%">
Gets data from the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-getsegmentdatacount">GetSegmentDataCount</a>
</td>
<td align="left" width="63%">
Gets the size of the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-removecommandsatend">RemoveCommandsAtEnd</a>
</td>
<td align="left" width="63%">
Removes commands from the end of the commands array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-removesegmentdataatend">RemoveSegmentDataAtEnd</a>
</td>
<td align="left" width="63%">
Removes data from the end of the segment data array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-updatecommands">UpdateCommands</a>
</td>
<td align="left" width="63%">
Updates the commands array. Existing commands not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgpathdata-updatesegmentdata">UpdateSegmentData</a>
</td>
<td align="left" width="63%">
Updates the segment data array. Existing segment data not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new segment data.

</td>
</tr>
</table> 

