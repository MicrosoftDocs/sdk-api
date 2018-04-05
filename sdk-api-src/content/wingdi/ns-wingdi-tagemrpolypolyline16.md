---
UID: NS:wingdi.tagEMRPOLYPOLYLINE16
title: tagEMRPOLYPOLYLINE16
author: windows-driver-content
description: The EMRPOLYPOLYLINE16 and EMRPOLYPOLYGON16 structures contain members for the PolyPolyline and PolyPolygon enhanced metafile records.
old-location: gdi\emrpolypolyline16__emrpolypolygon16.htm
old-project: gdi
ms.assetid: efdd4ed1-5c0e-43ae-980d-fe3a5e8d480f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PEMRPOLYPOLYGON16, *PEMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, EMRPOLYPOLYGON16 structure [Windows GDI], EMRPOLYPOLYLINE16, EMRPOLYPOLYLINE16 structure [Windows GDI], EMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, EMRPOLYPOLYLINE16, EMRPOLYPOLYGON16 structure [Windows GDI], PEMRPOLYPOLYGON16, PEMRPOLYPOLYGON16 structure pointer [Windows GDI], PEMRPOLYPOLYLINE16, PEMRPOLYPOLYLINE16 structure pointer [Windows GDI], _win32_EMRPOLYPOLYLINE16_str, gdi.emrpolypolyline16__emrpolypolygon16, tagEMRPOLYPOLYLINE16, wingdi/EMRPOLYPOLYGON16, wingdi/EMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, wingdi/PEMRPOLYPOLYGON16, wingdi/PEMRPOLYPOLYLINE16"
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
req.typenames: EMRPOLYPOLYLINE16, *PEMRPOLYPOLYLINE16, EMRPOLYPOLYGON16, *PEMRPOLYPOLYGON16
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRPOLYPOLYLINE16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRPOLYPOLYLINE16 structure


## -description



The <b>EMRPOLYPOLYLINE16</b> and <b>EMRPOLYPOLYGON16</b> structures contain members for the <a href="https://msdn.microsoft.com/71a9273f-321b-4efb-ac73-5979f8151d05">PolyPolyline</a> and <a href="https://msdn.microsoft.com/ac0a2802-c8b0-4cd7-9521-5b179f2c70b9">PolyPolygon</a> enhanced metafile records.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field nPolys

The number of polys.


### -field cpts

The total number of points in all polys.


### -field aPolyCounts

An array of point counts for each poly.


### -field apts

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a> structures, representing the points in logical units.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>
 

 

