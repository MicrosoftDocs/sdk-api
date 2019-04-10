---
UID: NF:winddi.PATHOBJ_vGetBounds
title: PATHOBJ_vGetBounds function (winddi.h)
author: windows-sdk-content
description: The PATHOBJ_vGetBounds function retrieves the bounding rectangle for the specified path.
old-location: display\pathobj_vgetbounds.htm
tech.root: display
ms.assetid: f7ce7909-552c-4e23-a620-280fadeade01
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PATHOBJ_vGetBounds, PATHOBJ_vGetBounds function [Display Devices], display.pathobj_vgetbounds, gdifncs_d5ad1bbf-ddbe-43c1-92a9-dbe3a0091b24.xml, winddi/PATHOBJ_vGetBounds
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
 - PATHOBJ_vGetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PATHOBJ_vGetBounds function


## -description


The <b>PATHOBJ_vGetBounds</b> function retrieves the bounding rectangle for the specified path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that describes the path for which a bounding rectangle is to be calculated.


### -param prectfx

Pointer to the address where the RECTFX structure is to be written. The returned rectangle is exclusive of the bottom and right edges. An empty rectangle is specified by setting all four RECTFX members to zero. For a description of this data type, see <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a>.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>
 

 

