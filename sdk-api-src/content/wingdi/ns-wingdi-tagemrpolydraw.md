---
UID: NS:wingdi.tagEMRPOLYDRAW
title: tagEMRPOLYDRAW
author: windows-sdk-content
description: The EMRPOLYDRAW structure contains members for the PolyDraw enhanced metafile record.
old-location: gdi\emrpolydraw.htm
tech.root: gdi
ms.assetid: c75d19bf-a7e3-45db-9534-f089d4cec3eb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PEMRPOLYDRAW, EMRPOLYDRAW, EMRPOLYDRAW structure [Windows GDI], PEMRPOLYDRAW, PEMRPOLYDRAW structure pointer [Windows GDI], _win32_EMRPOLYDRAW_str, gdi.emrpolydraw, tagEMRPOLYDRAW, wingdi/EMRPOLYDRAW, wingdi/PEMRPOLYDRAW"
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
 - EMRPOLYDRAW
product: Windows
targetos: Windows
req.typenames: EMRPOLYDRAW, *PEMRPOLYDRAW
req.redist: 
---

# tagEMRPOLYDRAW structure


## -description



The <b>EMRPOLYDRAW</b> structure contains members for the <a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field rclBounds

The bounding rectangle, in device units.


### -field cptl

The number of points.


### -field aptl

An array of <a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a> structures, representing the data points in logical units.


### -field abTypes

An array of values that specifies how each point in the <b>aptl</b> array is used. Each element can be one of the following values: PT_MOVETO, PT_LINETO, or PT_BEZIERTO. The PT_LINETO or PT_BEZIERTO value can be combined with the PT_CLOSEFIGURE value using the bitwise-OR operator.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/587d36c8-e81c-4256-af25-af2a82727e8d">POINTL</a>



<a href="https://msdn.microsoft.com/5fd3f285-dcf3-4cd0-915a-236ba7902353">PolyDraw</a>



<a href="https://msdn.microsoft.com/47a89d2d-4733-47be-91c1-450845e78075">RECTL</a>
 

 

