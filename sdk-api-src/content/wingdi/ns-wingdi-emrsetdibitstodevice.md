---
UID: NS:wingdi.tagEMRSETDIBITSTODEVICE
title: EMRSETDIBITSTODEVICE
author: windows-sdk-content
description: The EMRSETDIBITSTODEVICE structure contains members for the SetDIBitsToDevice enhanced metafile record.
old-location: gdi\emrsetdibitstodevice.htm
tech.root: gdi
ms.assetid: a87546e4-32ce-438d-9997-6d329f43303e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEMRSETDIBITSTODEVICE, EMRSETDIBITSTODEVICE, EMRSETDIBITSTODEVICE structure [Windows GDI], PEMRSETDIBITSTODEVICE, PEMRSETDIBITSTODEVICE structure pointer [Windows GDI], _win32_EMRSETDIBITSTODEVICE_str, gdi.emrsetdibitstodevice, wingdi/EMRSETDIBITSTODEVICE, wingdi/PEMRSETDIBITSTODEVICE"
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
 - EMRSETDIBITSTODEVICE
product: Windows
targetos: Windows
req.typenames: EMRSETDIBITSTODEVICE, *PEMRSETDIBITSTODEVICE
req.redist: 
---

# EMRSETDIBITSTODEVICE structure


## -description



The <b>EMRSETDIBITSTODEVICE</b> structure contains members for the <a href="https://msdn.microsoft.com/41225400-12e3-47ba-8b88-ac1d5b0fa90f">SetDIBitsToDevice</a> enhanced metafile record.




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

Logical x-coordinate of the lower-left corner of the source device-independent bitmap (DIB).


### -field ySrc

Logical y-coordinate of the lower-left corner of the source DIB.


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


### -field iStartScan

First scan line in the array.


### -field cScans

Number of scan lines.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/41225400-12e3-47ba-8b88-ac1d5b0fa90f">SetDIBitsToDevice</a>
 

 

