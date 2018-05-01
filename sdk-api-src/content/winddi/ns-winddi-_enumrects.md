---
UID: NS:winddi._ENUMRECTS
title: "_ENUMRECTS"
author: windows-driver-content
description: The ENUMRECTS structure is used by the CLIPOBJ_cEnumStart function to provide information about rectangles in a clip region for the CLIPOBJ_bEnum function.
old-location: display\enumrects.htm
old-project: display
ms.assetid: f7b8787f-f383-4cae-970e-8f4eb34b00da
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ENUMRECTS, ENUMRECTS structure [Display Devices], _ENUMRECTS, display.enumrects, grstrcts_8ea2422f-1b57-4a7a-be86-adca8b830a36.xml, winddi/ENUMRECTS
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
req.typenames: ENUMRECTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	ENUMRECTS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _ENUMRECTS structure


## -description


The ENUMRECTS structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539421">CLIPOBJ_cEnumStart</a> function to provide information about rectangles in a clip region for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff539420">CLIPOBJ_bEnum</a> function.


## -struct-fields




### -field c

Specifies the number of RECTL structures in the <b>arcl</b> array.


### -field arcl

Is an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structures that specify the coordinates of rectangles in the clip region.

