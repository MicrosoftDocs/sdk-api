---
UID: NF:winddi.PATHOBJ_bEnum
title: PATHOBJ_bEnum function (winddi.h)
author: windows-sdk-content
description: The PATHOBJ_bEnum function retrieves the next PATHDATA record from a specified path and enumerates the curves in the path.
old-location: display\pathobj_benum.htm
tech.root: display
ms.assetid: 2e8bd76c-5ee6-4fe5-b1e5-64e84d09fc8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PATHOBJ_bEnum, PATHOBJ_bEnum function [Display Devices], display.pathobj_benum, gdifncs_afa2e11c-1671-426c-aab8-c0998eafb4b5.xml, winddi/PATHOBJ_bEnum
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
 - PATHOBJ_bEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PATHOBJ_bEnum function


## -description


The <b>PATHOBJ_bEnum</b> function retrieves the next PATHDATA record from a specified path and enumerates the curves in the path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure whose curves and/or lines are to be enumerated.


### -param ppd

Pointer to a <a href="https://msdn.microsoft.com/ba86d245-1ec2-42aa-9502-256981109700">PATHDATA</a> structure that is to be filled.


## -returns



The return value is <b>TRUE</b> if the specified path contains more PATHDATA records, indicating that this service should be called again. Otherwise, if the output is the last PATHDATA record in the path, the return value is <b>FALSE</b>.




## -remarks



<b>PATHOBJ_bEnum</b> can be called only after a call to <a href="https://msdn.microsoft.com/b83e6f87-be79-4743-bc52-b9310853c4f5">PATHOBJ_vEnumStart</a> has been made.

A PATHDATA structure describes all or part of a subpath (a connected part of a path). For example, a <b>MoveTo</b> call by the application within a path begins a new subpath.




## -see-also




<a href="https://msdn.microsoft.com/ba86d245-1ec2-42aa-9502-256981109700">PATHDATA</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/b83e6f87-be79-4743-bc52-b9310853c4f5">PATHOBJ_vEnumStart</a>



<a href="https://msdn.microsoft.com/3db437aa-40d1-4703-ab1e-b3e154923d2d">PATHOBJ_vEnumStartClipLines</a>
 

 

