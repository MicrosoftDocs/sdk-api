---
UID: NF:d2d1svg.ID2D1SvgPathData.GetCommands
title: ID2D1SvgPathData::GetCommands (d2d1svg.h)
description: Gets commands from the commands array.
helpviewer_keywords: ["GetCommands","GetCommands method [Direct2D]","GetCommands method [Direct2D]","ID2D1SvgPathData interface","ID2D1SvgPathData interface [Direct2D]","GetCommands method","ID2D1SvgPathData.GetCommands","ID2D1SvgPathData::GetCommands","d2d1svg/ID2D1SvgPathData::GetCommands","direct2d.id2d1svgpathdata_getcommands"]
old-location: direct2d\id2d1svgpathdata_getcommands.htm
tech.root: Direct2D
ms.assetid: D72199E5-11E5-413E-88F0-85EF17585587
ms.date: 12/05/2018
ms.keywords: GetCommands, GetCommands method [Direct2D], GetCommands method [Direct2D],ID2D1SvgPathData interface, ID2D1SvgPathData interface [Direct2D],GetCommands method, ID2D1SvgPathData.GetCommands, ID2D1SvgPathData::GetCommands, d2d1svg/ID2D1SvgPathData::GetCommands, direct2d.id2d1svgpathdata_getcommands
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgPathData::GetCommands
 - d2d1svg/ID2D1SvgPathData::GetCommands
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgPathData.GetCommands
---

# ID2D1SvgPathData::GetCommands


## -description

Gets commands from the commands array.

## -parameters

### -param commands [out]

Type: <b><a href="/windows/desktop/api/d2d1svg/ne-d2d1svg-d2d1_svg_path_command">D2D1_SVG_PATH_COMMAND</a>*</b>

Buffer to contain the commands.

### -param commandsCount

Type: <b>UINT32</b>

The element count of the buffer.

### -param startIndex

Type: <b>UINT32</b>

The index of the first commands to retrieve.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgpathdata">ID2D1SvgPathData</a>