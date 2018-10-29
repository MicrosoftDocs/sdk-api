---
UID: NS:wingdi.tagEMRCREATEMONOBRUSH
title: tagEMRCREATEMONOBRUSH
author: windows-sdk-content
description: The EMRCREATEMONOBRUSH structure contains members for the CreatePatternBrush (when passed a monochrome bitmap) or CreateDIBPatternBrush (when passed a monochrome DIB) enhanced metafile records.
old-location: gdi\emrcreatemonobrush.htm
tech.root: gdi
ms.assetid: 6f581ad4-0449-40b1-bcc6-737bfcdc33c4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PEMRCREATEMONOBRUSH, EMRCREATEMONOBRUSH, EMRCREATEMONOBRUSH structure [Windows GDI], PEMRCREATEMONOBRUSH, PEMRCREATEMONOBRUSH structure pointer [Windows GDI], _win32_EMRCREATEMONOBRUSH_str, gdi.emrcreatemonobrush, tagEMRCREATEMONOBRUSH, wingdi/EMRCREATEMONOBRUSH, wingdi/PEMRCREATEMONOBRUSH"
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
 - EMRCREATEMONOBRUSH
product: Windows
targetos: Windows
req.typenames: EMRCREATEMONOBRUSH, *PEMRCREATEMONOBRUSH
req.redist: 
---

# tagEMRCREATEMONOBRUSH structure


## -description



The <b>EMRCREATEMONOBRUSH</b> structure contains members for the <a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a> (when passed a monochrome bitmap) or <a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a> (when passed a monochrome DIB) enhanced metafile records.




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



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

