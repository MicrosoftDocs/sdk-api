---
UID: NS:winddi._BLENDOBJ
title: "_BLENDOBJ"
author: windows-sdk-content
description: The BLENDOBJ structure controls blending by specifying the blending functions for source and destination bitmaps.
old-location: display\blendobj.htm
old-project: display
ms.assetid: 1bbe5cb6-8722-45bb-ae43-01bc4460f08d
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*PBLENDOBJ, BLENDOBJ, BLENDOBJ structure [Display Devices], PBLENDOBJ, PBLENDOBJ structure pointer [Display Devices], _BLENDOBJ, display.blendobj, grstrcts_0d4470ae-12b0-41f4-8209-49b346e4829d.xml, winddi/BLENDOBJ, winddi/PBLENDOBJ"
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
tech.root: 
req.typenames: BLENDOBJ, *PBLENDOBJ
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - BLENDOBJ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _BLENDOBJ structure


## -description


The BLENDOBJ structure controls blending by specifying the blending functions for source and destination bitmaps. 


## -struct-fields




### -field BlendFunction

Is a BLENDFUNCTION structure (described in the Microsoft Window SDK documentation) that specifies the blending operation to use, the alpha transparency for the source bitmap, and the way the source and destination bitmaps are interpreted.

