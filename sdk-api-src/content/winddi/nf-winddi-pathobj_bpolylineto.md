---
UID: NF:winddi.PATHOBJ_bPolyLineTo
title: PATHOBJ_bPolyLineTo function
author: windows-sdk-content
description: The PATHOBJ_bPolyLineTo function draws lines from the current position in a path through the specified points.
old-location: display\pathobj_bpolylineto.htm
tech.root: display
ms.assetid: 468d20e3-a78b-47b3-9c56-ef355181eb63
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: PATHOBJ_bPolyLineTo, PATHOBJ_bPolyLineTo function [Display Devices], display.pathobj_bpolylineto, gdifncs_eaa54bcf-8b39-4661-a2cf-79198ffa1df6.xml, winddi/PATHOBJ_bPolyLineTo
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
 - PATHOBJ_bPolyLineTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PATHOBJ_bPolyLineTo function


## -description


The <b>PATHOBJ_bPolyLineTo</b> function draws lines from the current position in a path through the specified points.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure created by the driver.


### -param pptfx

Pointer to an array of POINTFIX structures that define control points. The first line is drawn from the current position to the first point in this array; lines are then drawn to each subsequent point in the array. For a description of this data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


### -param cptfx

Specifies the count of points in <i>pptfx</i>. This is also the number of lines that will be added to the path.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



<b>PATHOBJ_bPolyLineTo</b> should only be called with PATHOBJ structures created by <a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>.




## -see-also




<a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/0937c816-b205-4c5d-b4b6-74c3e7fdb0ce">PATHOBJ_bPolyBezierTo</a>
 

 

