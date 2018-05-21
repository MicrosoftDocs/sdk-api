---
UID: NS:winddi._FONTSIM
title: "_FONTSIM"
author: windows-driver-content
description: The FONTSIM structure contains offsets to one or more FONTDIFF structures describing bold, italic, and bold italic font simulations.
old-location: display\fontsim.htm
old-project: display
ms.assetid: 46d4170e-13d6-406f-991f-2024fadd8ddc
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: FONTSIM, FONTSIM structure [Display Devices], _FONTSIM, display.fontsim, grstrcts_b6931468-edd5-4675-a8e2-a594741f7e6c.xml, winddi/FONTSIM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
req.typenames: FONTSIM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	FONTSIM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FONTSIM structure


## -description


The FONTSIM structure contains offsets to one or more <a href="https://msdn.microsoft.com/library/windows/hardware/ff565967">FONTDIFF</a> structures describing bold, italic, and bold italic font simulations.


## -struct-fields




### -field dpBold

If nonzero, specifies the offset from the beginning of this structure to the FONTDIFF structure describing the bold simulation. If this member is zero, the font does not support bold simulation.


### -field dpItalic

If nonzero, specifies the offset from the beginning of this structure to the FONTDIFF structure describing the italic simulation. If this member is zero, the font does not support italic simulation.


### -field dpBoldItalic

If nonzero, specifies the offset from the beginning of this structure to the FONTDIFF structure describing the bold italic simulation. If this member is zero, the font does not support bold italic simulation.


## -remarks



If the <b>dpFontSim</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a> structure is nonzero, it holds the offset from the beginning of that structure to the beginning of a FONTSIM structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565967">FONTDIFF</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>
 

 

