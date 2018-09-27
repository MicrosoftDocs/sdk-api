---
UID: NS:wingdi._RGNDATA
title: "_RGNDATA"
author: windows-sdk-content
description: The RGNDATA structure contains a header and an array of rectangles that compose a region. The rectangles are sorted top to bottom, left to right. They do not overlap.
old-location: gdi\rgndata.htm
tech.root: gdi
ms.assetid: 3eac0b23-3138-4b34-9c16-6cc185e4de22
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*LPRGNDATA, *NPRGNDATA, *PRGNDATA, PRGNDATA, PRGNDATA structure pointer [Windows GDI], RGNDATA, RGNDATA structure [Windows GDI], _RGNDATA, _win32_RGNDATA_str, gdi.rgndata, wingdi/PRGNDATA, wingdi/RGNDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGNDATA
product: Windows
targetos: Windows
req.typenames: RGNDATA, *PRGNDATA, *NPRGNDATA, *LPRGNDATA
req.redist: 
---

# _RGNDATA structure


## -description



The <b>RGNDATA</b> structure contains a header and an array of rectangles that compose a region. The rectangles are sorted top to bottom, left to right. They do not overlap.




## -struct-fields




### -field rdh

A <a href="https://msdn.microsoft.com/15990903-8a48-4c47-b527-269d775255a5">RGNDATAHEADER</a> structure. The members of this structure specify the type of region (whether it is rectangular or trapezoidal), the number of rectangles that make up the region, the size of the buffer that contains the rectangle structures, and so on.


### -field Buffer

Specifies an arbitrary-size buffer that contains the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures that make up the region.


## -see-also




<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/15990903-8a48-4c47-b527-269d775255a5">RGNDATAHEADER</a>



<a href="https://msdn.microsoft.com/e66d46fd-af6f-43ce-a9f7-21389d14cb89">Region Structures</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

