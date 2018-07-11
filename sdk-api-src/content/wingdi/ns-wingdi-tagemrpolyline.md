---
UID: NS:wingdi.tagEMRPOLYLINE
title: tagEMRPOLYLINE
author: windows-sdk-content
description: The EMRPOLYLINE, EMRPOLYBEZIER, EMRPOLYGON, EMRPOLYBEZIERTO, and EMRPOLYLINETO structures contain members for the Polyline, PolyBezier, Polygon, PolyBezierTo, and PolylineTo enhanced metafile records.
old-location: gdi\emrpolyline__emrpolybezier__emrpolygon__emrpolybezierto__emrpolylineto.htm
old-project: gdi
ms.assetid: 47a05287-8950-4277-b981-a19bff918bae
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PEMRPOLYBEZIER, *PEMRPOLYBEZIERTO, *PEMRPOLYGON, *PEMRPOLYLINE, *PEMRPOLYLINETO, EMRPOLYBEZIER, EMRPOLYBEZIER structure [Windows GDI], EMRPOLYBEZIERTO, EMRPOLYBEZIERTO structure [Windows GDI], EMRPOLYGON, EMRPOLYGON structure [Windows GDI], EMRPOLYLINE, EMRPOLYLINE structure [Windows GDI], EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO, EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO structure [Windows GDI], EMRPOLYLINETO, EMRPOLYLINETO structure [Windows GDI], PEMRPOLYBEZIER, PEMRPOLYBEZIER structure pointer [Windows GDI], PEMRPOLYBEZIERTO, PEMRPOLYBEZIERTO structure pointer [Windows GDI], PEMRPOLYGON, PEMRPOLYGON structure pointer [Windows GDI], PEMRPOLYLINE, PEMRPOLYLINE structure pointer [Windows GDI], PEMRPOLYLINETO, PEMRPOLYLINETO structure pointer [Windows GDI], _win32_EMRPOLYLINE_str, gdi.emrpolyline__emrpolybezier__emrpolygon__emrpolybezierto__emrpolylineto, tagEMRPOLYLINE, wingdi/EMRPOLYBEZIER, wingdi/EMRPOLYBEZIERTO, wingdi/EMRPOLYGON, wingdi/EMRPOLYLINE,EMRPOLYBEZIER,EMRPOLYGON,EMRPOLYBEZIERTO,EMRPOLYLINETO, wingdi/EMRPOLYLINETO, wingdi/PEMRPOLYBEZIER, wingdi/PEMRPOLYBEZIERTO, wingdi/PEMRPOLYGON, wingdi/PEMRPOLYLINE, wingdi/PEMRPOLYLINETO"
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
req.typenames: EMRPOLYLINE, *PEMRPOLYLINE, EMRPOLYBEZIER, *PEMRPOLYBEZIER, EMRPOLYGON, *PEMRPOLYGON, EMRPOLYBEZIERTO, *PEMRPOLYBEZIERTO, EMRPOLYLINETO, *PEMRPOLYLINETO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRPOLYLINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRPOLYLINE structure


## -description



The <b>EMRPOLYLINE, </b><b>EMRPOLYBEZIER, </b><b>EMRPOLYGON, </b><b>EMRPOLYBEZIERTO, </b> and <b>EMRPOLYLINETO</b> structures contain members for the <a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>, <a href="https://msdn.microsoft.com/d1622574-c65e-4265-9a17-22bb4d2cae0e">PolyBezier</a>, <a href="https://msdn.microsoft.com/2f958b91-039a-4e02-b727-be142bb18b06">Polygon</a>, <a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a>, and <a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field rclBounds

Bounding rectangle, in device units.


### -field cptl

Number of points array.


### -field aptl

Array of 32-bit points, in logical units.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

