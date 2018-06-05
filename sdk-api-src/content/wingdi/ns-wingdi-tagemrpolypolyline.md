---
UID: NS:wingdi.tagEMRPOLYPOLYLINE
title: tagEMRPOLYPOLYLINE
author: windows-sdk-content
description: The EMRPOLYPOLYLINE and EMRPOLYPOLYGON structures contain members for the PolyPolyline and PolyPolygon enhanced metafile records.
old-location: gdi\emrpolypolyline__emrpolypolygon.htm
old-project: gdi
ms.assetid: 442ad347-c064-4769-b43b-57d2e66e8b97
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PEMRPOLYPOLYGON, *PEMRPOLYPOLYLINE, EMRPOLYPOLYGON, EMRPOLYPOLYGON structure [Windows GDI], EMRPOLYPOLYLINE, EMRPOLYPOLYLINE structure [Windows GDI], EMRPOLYPOLYLINE,EMRPOLYPOLYGON, EMRPOLYPOLYLINE,EMRPOLYPOLYGON structure [Windows GDI], PEMRPOLYPOLYGON, PEMRPOLYPOLYGON structure pointer [Windows GDI], PEMRPOLYPOLYLINE, PEMRPOLYPOLYLINE structure pointer [Windows GDI], _win32_EMRPOLYPOLYLINE_str, gdi.emrpolypolyline__emrpolypolygon, tagEMRPOLYPOLYLINE, wingdi/EMRPOLYPOLYGON, wingdi/EMRPOLYPOLYLINE,EMRPOLYPOLYGON, wingdi/PEMRPOLYPOLYGON, wingdi/PEMRPOLYPOLYLINE"
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
req.typenames: EMRPOLYPOLYLINE, *PEMRPOLYPOLYLINE, EMRPOLYPOLYGON, *PEMRPOLYPOLYGON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRPOLYPOLYLINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRPOLYPOLYLINE structure


## -description



The <b>EMRPOLYPOLYLINE</b> and <b>EMRPOLYPOLYGON</b> structures contain members for the <a href="https://msdn.microsoft.com/71a9273f-321b-4efb-ac73-5979f8151d05">PolyPolyline</a> and <a href="https://msdn.microsoft.com/ac0a2802-c8b0-4cd7-9521-5b179f2c70b9">PolyPolygon</a> enhanced metafile records.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field nPolys

The number of polys.


### -field cptl

The total number of points in all polys.


### -field aPolyCounts

An array of point counts for each poly.


### -field aptl

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structures, representing the points in logical units.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>
 

 

