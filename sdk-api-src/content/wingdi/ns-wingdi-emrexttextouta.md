---
UID: NS:wingdi.tagEMREXTTEXTOUTA
title: EMREXTTEXTOUTA
author: windows-sdk-content
description: The EMREXTTEXTOUTA and EMREXTTEXTOUTW structures contain members for the ExtTextOut, TextOut, or DrawText enhanced metafile records.
old-location: gdi\emrexttextouta__emrexttextoutw.htm
tech.root: gdi
ms.assetid: 1d9b0b32-6a51-481a-9589-3de832d746d7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEMREXTTEXTOUTA, *PEMREXTTEXTOUTW, EMREXTTEXTOUTA, EMREXTTEXTOUTA structure [Windows GDI], EMREXTTEXTOUTA,EMREXTTEXTOUTW, EMREXTTEXTOUTA,EMREXTTEXTOUTW structure [Windows GDI], EMREXTTEXTOUTW, EMREXTTEXTOUTW structure [Windows GDI], PEMREXTTEXTOUTA, PEMREXTTEXTOUTA structure pointer [Windows GDI], PEMREXTTEXTOUTW, PEMREXTTEXTOUTW structure pointer [Windows GDI], _win32_EMREXTTEXTOUTA_str, gdi.emrexttextouta__emrexttextoutw, wingdi/EMREXTTEXTOUTA,EMREXTTEXTOUTW, wingdi/EMREXTTEXTOUTW, wingdi/PEMREXTTEXTOUTA, wingdi/PEMREXTTEXTOUTW"
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
 - EMREXTTEXTOUTA
product: Windows
targetos: Windows
req.typenames: EMREXTTEXTOUTA, *PEMREXTTEXTOUTA, EMREXTTEXTOUTW, *PEMREXTTEXTOUTW
req.redist: 
---

# EMREXTTEXTOUTA structure


## -description



The <b>EMREXTTEXTOUTA</b> and <b>EMREXTTEXTOUTW</b> structures contain members for the <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>, <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>, or <a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a> enhanced metafile records.




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


### -field emrtext

<b>EMRTEXT</b> structure, which is followed by the string and the intercharacter spacing array.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

