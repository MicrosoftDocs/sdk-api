---
UID: NS:winddi._ENUMRECTS
title: "_ENUMRECTS"
author: windows-sdk-content
description: The ENUMRECTS structure is used by the CLIPOBJ_cEnumStart function to provide information about rectangles in a clip region for the CLIPOBJ_bEnum function.
old-location: display\enumrects.htm
tech.root: display
ms.assetid: f7b8787f-f383-4cae-970e-8f4eb34b00da
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ENUMRECTS, ENUMRECTS structure [Display Devices], _ENUMRECTS, display.enumrects, grstrcts_8ea2422f-1b57-4a7a-be86-adca8b830a36.xml, winddi/ENUMRECTS
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - ENUMRECTS
product: Windows
targetos: Windows
req.typenames: ENUMRECTS
req.redist: 
---

# _ENUMRECTS structure


## -description


The ENUMRECTS structure is used by the <a href="https://msdn.microsoft.com/e719f856-04a9-480d-b79a-df2307a48162">CLIPOBJ_cEnumStart</a> function to provide information about rectangles in a clip region for the <a href="https://msdn.microsoft.com/d54e6e2a-4869-45d6-9ad1-4e9aca5f5e77">CLIPOBJ_bEnum</a> function.


## -struct-fields




### -field c

Specifies the number of RECTL structures in the <b>arcl</b> array.


### -field arcl

Is an array of <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structures that specify the coordinates of rectangles in the clip region.

