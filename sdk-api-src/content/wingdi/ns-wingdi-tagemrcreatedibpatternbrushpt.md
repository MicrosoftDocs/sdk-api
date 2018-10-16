---
UID: NS:wingdi.tagEMRCREATEDIBPATTERNBRUSHPT
title: tagEMRCREATEDIBPATTERNBRUSHPT
author: windows-sdk-content
description: The EMRCREATEDIBPATTERNBRUSHPT structure contains members for the CreateDIBPatternBrushPt enhanced metafile record. The BITMAPINFO structure is followed by the bitmap bits that form a packed device-independent bitmap (DIB).
old-location: gdi\emrcreatedibpatternbrushpt.htm
tech.root: gdi
ms.assetid: e1d8302b-9dbe-4a92-9143-7ad03e334ee5
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PEMRCREATEDIBPATTERNBRUSHPT, *PEMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI], EMRCREATEDIBPATTERNBRUSHPT, EMRCREATEDIBPATTERNBRUSHPT structure [Windows GDI], _win32_EMRCREATEDIBPATTERNBRUSHPT_str, gdi.emrcreatedibpatternbrushpt, tagEMRCREATEDIBPATTERNBRUSHPT, wingdi/*PEMRCREATEDIBPATTERNBRUSHPT, wingdi/EMRCREATEDIBPATTERNBRUSHPT"
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
 - EMRCREATEDIBPATTERNBRUSHPT
product: Windows
targetos: Windows
req.typenames: EMRCREATEDIBPATTERNBRUSHPT, *PEMRCREATEDIBPATTERNBRUSHPT
req.redist: 
---

# tagEMRCREATEDIBPATTERNBRUSHPT structure


## -description



The <b>EMRCREATEDIBPATTERNBRUSHPT</b> structure contains members for the <a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a> enhanced metafile record. The <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure is followed by the bitmap bits that form a packed device-independent bitmap (DIB).




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihBrush

Index of brush in handle table.


### -field iUsage

Value specifying whether the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure was provided and, if so, whether <b>bmiColors</b> contains explicit red, green, blue (RGB) values or indices. The <b>iUsage</b> member must be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.


### -field offBmi

Offset to <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field cbBmi

Size of <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field offBits

Offset to bitmap bits.


### -field cbBits

Size of bitmap bits.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/0e34d108-fd35-4512-9eb3-c7710af36e95">CreateDIBPatternBrushPt</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

