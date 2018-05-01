---
UID: NS:wingdi.tagEMRSTRETCHDIBITS
title: tagEMRSTRETCHDIBITS
author: windows-driver-content
description: The EMRSTRETCHDIBITS structure contains members for the StretchDIBits enhanced metafile record.
old-location: gdi\emrstretchdibits.htm
old-project: gdi
ms.assetid: aa104ffa-44ed-41f6-a1a7-23bbab68e16c
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PEMRSTRETCHDIBITS, EMRSTRETCHDIBITS, EMRSTRETCHDIBITS structure [Windows GDI], PEMRSTRETCHDIBITS, PEMRSTRETCHDIBITS structure pointer [Windows GDI], _win32_EMRSTRETCHDIBITS_str, gdi.emrstretchdibits, tagEMRSTRETCHDIBITS, wingdi/EMRSTRETCHDIBITS, wingdi/PEMRSTRETCHDIBITS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: EMRSTRETCHDIBITS, *PEMRSTRETCHDIBITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRSTRETCHDIBITS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRSTRETCHDIBITS structure


## -description



The <b>EMRSTRETCHDIBITS</b> structure contains members for the <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field xDest

Logical x-coordinate of the upper-left corner of the destination rectangle.


### -field yDest

Logical y-coordinate of the upper-left corner of the destination rectangle.


### -field xSrc

Logical x-coordinate of the upper-left corner of the source rectangle.


### -field ySrc

Logical y-coordinate of the upper-left corner of the source rectangle.


### -field cxSrc

Width of the source rectangle, in logical units.


### -field cySrc

Height of the source rectangle, in logical units.


### -field offBmiSrc

Offset to the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field cbBmiSrc

Size of the source <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure.


### -field offBitsSrc

Offset to source bitmap bits.


### -field cbBitsSrc

Size of source bitmap bits.


### -field iUsageSrc

Value of the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. The <b>iUsageSrc</b> member can be either the DIB_PAL_COLORS or DIB_RGB_COLORS value.


### -field dwRop

Raster-operation code. These codes define how the color data of the source rectangle is to be combined with the color data of the destination rectangle to achieve the final color.


### -field cxDest

Logical width of the destination rectangle.


### -field cyDest

Logical height of the destination rectangle.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

