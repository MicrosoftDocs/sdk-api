---
UID: NS:lpmapi.__unnamed_struct_17
title: IntServParmHdr (lpmapi.h)
description: The IntServParmHdr structure is a header for Integrated Services parameters.
old-location: qos\intservparmhdr.htm
tech.root: QOS
ms.assetid: 56ca242e-d5e9-4c16-9c8e-70a356375683
ms.date: 12/05/2018
ms.keywords: IntServParmHdr, IntServParmHdr structure [QOS], lpmapi/IntServParmHdr, qos.intservparmhdr
f1_keywords:
- lpmapi/IntServParmHdr
dev_langs:
- c++
req.header: lpmapi.h
req.include-header: 
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
- Lpmapi.h
api_name:
- IntServParmHdr
targetos: Windows
req.typenames: IntServParmHdr
req.redist: 
ms.custom: 19H1
---

# IntServParmHdr structure


## -description


The 
<b>IntServParmHdr</b> structure is a header for Integrated Services parameters.


## -struct-fields




### -field isph_parm_num

Parameter number of the attached object.


### -field isph_flags

Flags for the corresponding parameter object.


### -field isph_len32b

Number of 32-bit WORDs in the object, excluding this header object.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>
 

 

