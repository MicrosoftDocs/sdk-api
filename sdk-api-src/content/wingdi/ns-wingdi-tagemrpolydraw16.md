---
UID: NS:wingdi.tagEMRPOLYDRAW16
title: tagEMRPOLYDRAW16
author: windows-sdk-content
description: The EMRPOLYDRAW16 structure contains members for the PolyDraw enhanced metafile record.
old-location: gdi\emrpolydraw16.htm
old-project: gdi
ms.assetid: 476c5a81-99fc-4e25-a761-b95bbf18b271
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PEMRPOLYDRAW16, EMRPOLYDRAW16, EMRPOLYDRAW16 structure [Windows GDI], PEMRPOLYDRAW16, PEMRPOLYDRAW16 structure pointer [Windows GDI], _win32_EMRPOLYDRAW16_str, gdi.emrpolydraw16, tagEMRPOLYDRAW16, wingdi/EMRPOLYDRAW16, wingdi/PEMRPOLYDRAW16"
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
req.typenames: EMRPOLYDRAW16, *PEMRPOLYDRAW16
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRPOLYDRAW16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRPOLYDRAW16 structure


## -description



The <b>EMRPOLYDRAW16</b> structure contains members for the <a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field cpts

The number of points.


### -field apts

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a> structures, representing the data points in logical units.


### -field abTypes

An array of values that specifies how each point in the <b>apts</b> array is used. Each element can be one of the following values: PT_MOVETO, PT_LINETO, or PT_BEZIERTO. The PT_LINETO or PT_BEZIERTO value can be combined with the PT_CLOSEFIGURE value using the bitwise-OR operator.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569167">POINTS</a>



<a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>
 

 

