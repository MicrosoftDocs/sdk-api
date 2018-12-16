---
UID: NF:d2d1svg.ID2D1SvgPathData.GetCommands
title: ID2D1SvgPathData::GetCommands
author: windows-sdk-content
description: Gets commands from the commands array.
old-location: direct2d\id2d1svgpathdata_getcommands.htm
tech.root: direct2d
ms.assetid: D72199E5-11E5-413E-88F0-85EF17585587
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCommands, GetCommands method [Direct2D], GetCommands method [Direct2D],ID2D1SvgPathData interface, ID2D1SvgPathData interface [Direct2D],GetCommands method, ID2D1SvgPathData.GetCommands, ID2D1SvgPathData::GetCommands, d2d1svg/ID2D1SvgPathData::GetCommands, direct2d.id2d1svgpathdata_getcommands
ms.topic: method
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
 - ID2D1SvgPathData.GetCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgPathData::GetCommands


## -description


Gets commands from the commands array.


## -parameters




### -param commands [out]

Type: <b><a href="https://msdn.microsoft.com/E0A5F435-F4FB-4CD3-84B3-962CB7B96446">D2D1_SVG_PATH_COMMAND</a>*</b>

Buffer to contain the commands.


### -param commandsCount

Type: <b>UINT32</b>

The element count of the buffer.


### -param startIndex

Type: <b>UINT32</b>

The index of the first commands to retrieve.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/14879B17-0CAA-42E7-8643-7D385EABFD37">ID2D1SvgPathData</a>
 

 

