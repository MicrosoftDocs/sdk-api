---
UID: NS:wingdi.tagEMRTEXT
title: EMRTEXT (wingdi.h)
author: windows-sdk-content
description: The EMRTEXT structure contains members for text output.
old-location: gdi\emrtext.htm
tech.root: gdi
ms.assetid: a126f1ea-35ef-492d-8184-fb288a74f7f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMRTEXT, EMRTEXT, EMRTEXT structure [Windows GDI], PEMRTEXT, PEMRTEXT structure pointer [Windows GDI], _win32_EMRTEXT_str, gdi.emrtext, wingdi/EMRTEXT, wingdi/PEMRTEXT"
ms.topic: struct
f1_keywords: ["wingdi/EMRTEXT"]
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
 - EMRTEXT
product: Windows
targetos: Windows
req.typenames: EMRTEXT, *PEMRTEXT
req.redist: 
ms.custom: 19H1
---

# EMRTEXT structure


## -description



The <b>EMRTEXT</b> structure contains members for text output.




## -struct-fields




### -field ptlReference

The logical coordinates of the reference point used to position the string.


### -field nChars

The number of characters in the string.


### -field offString

The offset to the string.


### -field fOptions

A value that indicates how to use the application-defined rectangle. This member can be a combination of the ETO_CLIPPED and ETO_OPAQUE values.


### -field rcl

An optional clipping and/or opaquing rectangle, in logical units.


### -field offDx

The offset to the intercharacter spacing array.


## -remarks



The <b>EMRTEXT</b> structure is used as a member in the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrexttextouta">EMREXTTEXTOUT</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolytextouta">EMRPOLYTEXTOUT</a> structures.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemr">EMR</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions//dd162807(v=vs.85)">POINTL</a>



<a href="https://docs.microsoft.com/previous-versions//dd162907(v=vs.85)">RECTL</a>
 

 

