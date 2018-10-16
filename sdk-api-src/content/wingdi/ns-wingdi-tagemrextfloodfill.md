---
UID: NS:wingdi.tagEMREXTFLOODFILL
title: tagEMREXTFLOODFILL
author: windows-sdk-content
description: The EMREXTFLOODFILL structure contains members for the ExtFloodFill enhanced metafile record.
old-location: gdi\emrextfloodfill.htm
tech.root: gdi
ms.assetid: 93c80ea4-42f3-4c0a-8f72-76d2a6634e15
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PEMREXTFLOODFILL, EMREXTFLOODFILL, EMREXTFLOODFILL structure [Windows GDI], PEMREXTFLOODFILL, PEMREXTFLOODFILL structure pointer [Windows GDI], _win32_EMREXTFLOODFILL_str, gdi.emrextfloodfill, tagEMREXTFLOODFILL, wingdi/EMREXTFLOODFILL, wingdi/PEMREXTFLOODFILL"
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
 - EMREXTFLOODFILL
product: Windows
targetos: Windows
req.typenames: EMREXTFLOODFILL, *PEMREXTFLOODFILL
req.redist: 
---

# tagEMREXTFLOODFILL structure


## -description



The <b>EMREXTFLOODFILL</b> structure contains members for the <a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">ExtFloodFill</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ptlStart

Coordinates, in logical units, where filling begins.


### -field crColor

Color of fill. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


### -field iMode

Type of fill operation to be performed. This member must be either the FLOODFILLBORDER or FLOODFILLSURFACE value.


## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">ExtFloodFill</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

