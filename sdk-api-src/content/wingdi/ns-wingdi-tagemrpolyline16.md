---
UID: NS:wingdi.tagEMRPOLYLINE16
title: tagEMRPOLYLINE16
author: windows-driver-content
description: The EMRPOLYLINE16, EMRPOLYBEZIER16, EMRPOLYGON16, EMRPOLYBEZIERTO16, and EMRPOLYLINETO16 structures contain members for the Polyline, PolyBezier, Polygon, PolyBezierTo, and PolylineTo enhanced metafile records.
old-location: gdi\emrpolyline16__emrpolybezier16__emrpolygon16__emrpolybezierto16__emrpolylineto16.htm
old-project: gdi
ms.assetid: ba1d4fad-44d7-438c-8e03-972d88c2780e
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*PEMRPOLYBEZIER16, *PEMRPOLYBEZIERTO16, *PEMRPOLYGON16, *PEMRPOLYLINE16, *PEMRPOLYLINETO16, EMRPOLYBEZIER16, EMRPOLYBEZIER16 structure [Windows GDI], EMRPOLYBEZIERTO16, EMRPOLYBEZIERTO16 structure [Windows GDI], EMRPOLYGON16, EMRPOLYGON16 structure [Windows GDI], EMRPOLYLINE16, EMRPOLYLINE16 structure [Windows GDI], EMRPOLYLINE16,EMRPOLYBEZIER16,EMRPOLYGON16,EMRPOLYBEZIERTO16,EMRPOLYLINETO16, EMRPOLYLINE16,EMRPOLYBEZIER16,EMRPOLYGON16,EMRPOLYBEZIERTO16,EMRPOLYLINETO16 structure [Windows GDI], EMRPOLYLINETO16, EMRPOLYLINETO16 structure [Windows GDI], PEMRPOLYBEZIER16, PEMRPOLYBEZIER16 structure pointer [Windows GDI], PEMRPOLYBEZIERTO16, PEMRPOLYBEZIERTO16 structure pointer [Windows GDI], PEMRPOLYGON16, PEMRPOLYGON16 structure pointer [Windows GDI], PEMRPOLYLINE16, PEMRPOLYLINE16 structure pointer [Windows GDI], PEMRPOLYLINETO16, PEMRPOLYLINETO16 structure pointer [Windows GDI], _win32_EMRPOLYLINE16_str, gdi.emrpolyline16__emrpolybezier16__emrpolygon16__emrpolybezierto16__emrpolylineto16, tagEMRPOLYLINE16, wingdi/EMRPOLYBEZIER16, wingdi/EMRPOLYBEZIERTO16, wingdi/EMRPOLYGON16, wingdi/EMRPOLYLINE16,EMRPOLYBEZIER16,EMRPOLYGON16,EMRPOLYBEZIERTO16,EMRPOLYLINETO16, wingdi/EMRPOLYLINETO16, wingdi/PEMRPOLYBEZIER16, wingdi/PEMRPOLYBEZIERTO16, wingdi/PEMRPOLYGON16, wingdi/PEMRPOLYLINE16, wingdi/PEMRPOLYLINETO16"
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
req.typenames: EMRPOLYLINE16, *PEMRPOLYLINE16, EMRPOLYBEZIER16, *PEMRPOLYBEZIER16, EMRPOLYGON16, *PEMRPOLYGON16, EMRPOLYBEZIERTO16, *PEMRPOLYBEZIERTO16, EMRPOLYLINETO16, *PEMRPOLYLINETO16
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRPOLYLINE16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRPOLYLINE16 structure


## -description



The <b>EMRPOLYLINE16, </b><b>EMRPOLYBEZIER16, </b><b>EMRPOLYGON16, </b><b>EMRPOLYBEZIERTO16, </b> and <b>EMRPOLYLINETO16</b> structures contain members for the <a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>, <a href="https://msdn.microsoft.com/d1622574-c65e-4265-9a17-22bb4d2cae0e">PolyBezier</a>, <a href="https://msdn.microsoft.com/2f958b91-039a-4e02-b727-be142bb18b06">Polygon</a>, <a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a>, and <a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cpts

Number of points in the array.


### -field apts

Array of 16-bit points, in logical units.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

