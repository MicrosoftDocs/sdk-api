---
UID: NS:wingdi.tagEMRSETPIXELV
title: EMRSETPIXELV (wingdi.h)
author: windows-sdk-content
description: The EMRSETPIXELV structure contains members for the SetPixelV enhanced metafile record. When an enhanced metafile is created, calls to SetPixel are also recorded in this record.
old-location: gdi\emrsetpixelv.htm
tech.root: gdi
ms.assetid: 1487d788-c85a-4a58-a4c8-8abe198944b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRSETPIXELV, EMRSETPIXELV, EMRSETPIXELV structure [Windows GDI], PEMRSETPIXELV, PEMRSETPIXELV structure pointer [Windows GDI], _win32_EMRSETPIXELV_str, gdi.emrsetpixelv, wingdi/EMRSETPIXELV, wingdi/PEMRSETPIXELV"
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
 - EMRSETPIXELV
product: Windows
targetos: Windows
req.typenames: EMRSETPIXELV, *PEMRSETPIXELV
req.redist: 
ms.custom: 19H1
---

# EMRSETPIXELV structure


## -description



The <b>EMRSETPIXELV</b> structure contains members for the <a href="https://msdn.microsoft.com/638f0ffd-3771-4390-b335-0517be5312fd">SetPixelV</a> enhanced metafile record. When an enhanced metafile is created, calls to <a href="https://msdn.microsoft.com/652e2e7a-79ae-4668-b269-153ee08a5de9">SetPixel</a> are also recorded in this record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ptlPixel

Logical coordinates of pixel.


### -field crColor

Color value. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/652e2e7a-79ae-4668-b269-153ee08a5de9">SetPixel</a>



<a href="https://msdn.microsoft.com/638f0ffd-3771-4390-b335-0517be5312fd">SetPixelV</a>
 

 

