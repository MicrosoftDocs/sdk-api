---
UID: NF:winddi.PATHOBJ_bPolyBezierTo
title: PATHOBJ_bPolyBezierTo function
author: windows-sdk-content
description: The PATHOBJ_bPolyBezierTo function draws Bezier curves on a path.
old-location: display\pathobj_bpolybezierto.htm
tech.root: display
ms.assetid: 0937c816-b205-4c5d-b4b6-74c3e7fdb0ce
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PATHOBJ_bPolyBezierTo, PATHOBJ_bPolyBezierTo function [Display Devices], display.pathobj_bpolybezierto, gdifncs_787796de-11ca-457d-8084-8eb0af187eef.xml, winddi/PATHOBJ_bPolyBezierTo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - PATHOBJ_bPolyBezierTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PATHOBJ_bPolyBezierTo function


## -description


The <b>PATHOBJ_bPolyBezierTo</b> function draws Bezier curves on a path.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure created by the driver.


### -param pptfx

Pointer to the array of POINTFIX structures that define control points. Each set of three control points, along with the preceding control point, or current position, determines a Bezier curve. For a description of this data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -param cptfx

Specifies the count of points in <i>pptfx</i>. Must be a multiple of three.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



<b>PATHOBJ_bPolyBezierTo</b> must be called only with a PATHOBJ structure created by <a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>.




## -see-also




<a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/468d20e3-a78b-47b3-9c56-ef355181eb63">PATHOBJ_bPolyLineTo</a>
 

 

