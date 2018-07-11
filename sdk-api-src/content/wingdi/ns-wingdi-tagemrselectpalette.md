---
UID: NS:wingdi.tagEMRSELECTPALETTE
title: tagEMRSELECTPALETTE
author: windows-sdk-content
description: The EMRSELECTPALETTE structure contains members for the SelectPalette enhanced metafile record. Note that the bForceBackground parameter in SelectPalette is always recorded as TRUE, which causes the palette to be realized as a background palette.
old-location: gdi\emrselectpalette.htm
old-project: gdi
ms.assetid: f83367c0-406a-4a5f-961f-8e5afe6707fd
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PEMRSELECTPALETTE, EMRSELECTPALETTE, EMRSELECTPALETTE structure [Windows GDI], PEMRSELECTPALETTE, PEMRSELECTPALETTE structure pointer [Windows GDI], _win32_EMRSELECTPALETTE_str, gdi.emrselectpalette, tagEMRSELECTPALETTE, wingdi/EMRSELECTPALETTE, wingdi/PEMRSELECTPALETTE"
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
tech.root: 
req.typenames: EMRSELECTPALETTE, *PEMRSELECTPALETTE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRSELECTPALETTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRSELECTPALETTE structure


## -description



The <b>EMRSELECTPALETTE</b> structure contains members for the <a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a> enhanced metafile record. Note that the <i>bForceBackground</i> parameter in <b>SelectPalette</b> is always recorded as <b>TRUE</b>, which causes the palette to be realized as a background palette.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihPal

Index to logical palette in the handle table.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>
 

 

