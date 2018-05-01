---
UID: NS:wingdi.tagEMRFRAMERGN
title: tagEMRFRAMERGN
author: windows-driver-content
description: The EMRFRAMERGN structure contains members for the FrameRgn enhanced metafile record.
old-location: gdi\emrframergn.htm
old-project: gdi
ms.assetid: 578a2824-b42e-401d-b4b0-8426440713c6
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PEMRFRAMERGN, EMRFRAMERGN, EMRFRAMERGN structure [Windows GDI], PEMRFRAMERGN, PEMRFRAMERGN structure pointer [Windows GDI], _win32_EMRFRAMERGN_str, gdi.emrframergn, tagEMRFRAMERGN, wingdi/EMRFRAMERGN, wingdi/PEMRFRAMERGN"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: EMRFRAMERGN, *PEMRFRAMERGN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRFRAMERGN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRFRAMERGN structure


## -description



The <b>EMRFRAMERGN</b> structure contains members for the <a href="https://msdn.microsoft.com/d2c95392-7950-4963-8f10-2387daf23e93">FrameRgn</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cbRgnData

Size of region data, in bytes.


### -field ihBrush

Index of brush, in handle table.


### -field szlStroke

Width and height of region frame, in logical units.


### -field RgnData

Buffer containing <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/d2c95392-7950-4963-8f10-2387daf23e93">FrameRgn</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>
 

 

