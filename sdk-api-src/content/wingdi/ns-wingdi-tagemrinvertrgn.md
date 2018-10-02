---
UID: NS:wingdi.tagEMRINVERTRGN
title: tagEMRINVERTRGN
author: windows-sdk-content
description: The EMRINVERTRGN and EMRPAINTRGN structures contain members for the InvertRgn and PaintRgn enhanced metafile records.
old-location: gdi\emrinvertrgn__emrpaintrgn.htm
tech.root: gdi
ms.assetid: 91c0badc-bd26-418a-9cdb-3e70e7337021
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PEMRINVERTRGN, *PEMRPAINTRGN, EMRINVERTRGN, EMRINVERTRGN structure [Windows GDI], EMRINVERTRGN,EMRPAINTRGN, EMRINVERTRGN,EMRPAINTRGN structure [Windows GDI], EMRPAINTRGN, EMRPAINTRGN structure [Windows GDI], PEMRINVERTRGN, PEMRINVERTRGN structure pointer [Windows GDI], PEMRPAINTRGN, PEMRPAINTRGN structure pointer [Windows GDI], _win32_EMRINVERTRGN_str, gdi.emrinvertrgn__emrpaintrgn, tagEMRINVERTRGN, wingdi/EMRINVERTRGN,EMRPAINTRGN, wingdi/EMRPAINTRGN, wingdi/PEMRINVERTRGN, wingdi/PEMRPAINTRGN"
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
 - EMRINVERTRGN
product: Windows
targetos: Windows
req.typenames: EMRINVERTRGN, *PEMRINVERTRGN, EMRPAINTRGN, *PEMRPAINTRGN
req.redist: 
---

# tagEMRINVERTRGN structure


## -description



The <b>EMRINVERTRGN</b> and <b>EMRPAINTRGN</b> structures 
		  contain members for the <a href="https://msdn.microsoft.com/94704c44-796a-4ca7-97f3-6676d7f94078">InvertRgn</a> and <a href="https://msdn.microsoft.com/7656fb67-d865-459e-b379-4f2e44c76fd0">PaintRgn</a> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cbRgnData

Size of region data, in bytes.


### -field RgnData

Buffer containing an <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/94704c44-796a-4ca7-97f3-6676d7f94078">InvertRgn</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/7656fb67-d865-459e-b379-4f2e44c76fd0">PaintRgn</a>
 

 

