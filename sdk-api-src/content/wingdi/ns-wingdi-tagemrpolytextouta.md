---
UID: NS:wingdi.tagEMRPOLYTEXTOUTA
title: tagEMRPOLYTEXTOUTA
author: windows-sdk-content
description: The EMRPOLYTEXTOUTA and EMRPOLYTEXTOUTW structures contain members for the PolyTextOut enhanced metafile record.
old-location: gdi\emrpolytextouta__emrpolytextoutw.htm
tech.root: gdi
ms.assetid: 9c1decdd-fe6f-4220-abba-7547ab5427ba
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PEMRPOLYTEXTOUTA, *PEMRPOLYTEXTOUTW, EMRPOLYTEXTOUTA, EMRPOLYTEXTOUTA structure [Windows GDI], EMRPOLYTEXTOUTA,EMRPOLYTEXTOUTW, EMRPOLYTEXTOUTA,EMRPOLYTEXTOUTW structure [Windows GDI], EMRPOLYTEXTOUTW, EMRPOLYTEXTOUTW structure [Windows GDI], PEMRPOLYTEXTOUTA, PEMRPOLYTEXTOUTA structure pointer [Windows GDI], PEMRPOLYTEXTOUTW, PEMRPOLYTEXTOUTW structure pointer [Windows GDI], _win32_EMRPOLYTEXTOUTA_str, gdi.emrpolytextouta__emrpolytextoutw, tagEMRPOLYTEXTOUTA, wingdi/EMRPOLYTEXTOUTA,EMRPOLYTEXTOUTW, wingdi/EMRPOLYTEXTOUTW, wingdi/PEMRPOLYTEXTOUTA, wingdi/PEMRPOLYTEXTOUTW"
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
 - EMRPOLYTEXTOUTA
product: Windows
targetos: Windows
req.typenames: EMRPOLYTEXTOUTA, *PEMRPOLYTEXTOUTA, EMRPOLYTEXTOUTW, *PEMRPOLYTEXTOUTW
req.redist: 
---

# tagEMRPOLYTEXTOUTA structure


## -description



The <b>EMRPOLYTEXTOUTA</b> and <b>EMRPOLYTEXTOUTW</b> structures contain members for the <b>PolyTextOut</b> enhanced metafile record.




## -struct-fields




### -field emr

Base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field iGraphicsMode

Current graphics mode. This member can be either the GM_COMPATIBLE or GM_ADVANCED value.


### -field exScale

X-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.


### -field eyScale

Y-scaling factor from page units to .01mm units if the graphics mode is the GM_COMPATIBLE value.


### -field cStrings

Number of strings.


### -field aemrtext

<b>EMRTEXT</b> structure, which is followed by the string and the intercharacter spacing array.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

