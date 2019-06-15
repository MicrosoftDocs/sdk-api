---
UID: NF:d2d1svg.ID2D1SvgPathData.UpdateCommands
title: ID2D1SvgPathData::UpdateCommands (d2d1svg.h)
author: windows-sdk-content
description: Updates the commands array. Existing commands not updated by this method are preserved. The array is resized larger if necessary to accomodate the new commands.
old-location: direct2d\id2d1svgpathdata_updatecommands.htm
tech.root: Direct2D
ms.assetid: B6A6BC06-01C4-47D0-BC3C-7E0CE1A926F4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1SvgPathData interface [Direct2D],UpdateCommands method, ID2D1SvgPathData.UpdateCommands, ID2D1SvgPathData::UpdateCommands, UpdateCommands, UpdateCommands method [Direct2D], UpdateCommands method [Direct2D],ID2D1SvgPathData interface, d2d1svg/ID2D1SvgPathData::UpdateCommands, direct2d.id2d1svgpathdata_updatecommands
ms.topic: method
f1_keywords: ["d2d1svg/ID2D1SvgPathData.UpdateCommands"]
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
 - ID2D1SvgPathData.UpdateCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1SvgPathData::UpdateCommands


## -description


Updates the commands array. Existing commands not updated by this method are preserved. 
        The array is resized larger if necessary to accomodate the new commands.


## -parameters




### -param commands [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_path_command">D2D1_SVG_PATH_COMMAND</a>*</b>

The commands array.


### -param commandsCount

Type: <b>UINT32</b>

The number of commands to update.


### -param startIndex

Type: <b>UINT32</b>

The index at which to begin updating commands. Must be less than or equal to the size of the commands array.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpathdata">ID2D1SvgPathData</a>
 

 

