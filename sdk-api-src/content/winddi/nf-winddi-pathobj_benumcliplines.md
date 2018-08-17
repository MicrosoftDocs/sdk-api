---
UID: NF:winddi.PATHOBJ_bEnumClipLines
title: PATHOBJ_bEnumClipLines function
author: windows-sdk-content
description: The PATHOBJ_bEnumClipLines function enumerates clipped line segments from a given path.
old-location: display\pathobj_benumcliplines.htm
old-project: display
ms.assetid: edc64b1e-dd3f-4b6a-858c-91c49a819b0a
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: PATHOBJ_bEnumClipLines, PATHOBJ_bEnumClipLines function [Display Devices], display.pathobj_benumcliplines, gdifncs_39da05f4-124b-4d0f-b33b-777220462aa7.xml, winddi/PATHOBJ_bEnumClipLines
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - PATHOBJ_bEnumClipLines
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# PATHOBJ_bEnumClipLines function


## -description


The <b>PATHOBJ_bEnumClipLines</b> function enumerates clipped line segments from a given path. 


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure containing the clipped line segments that are to be enumerated.


### -param cb

Specifies the size of the output buffer, in bytes. GDI does not write beyond this point in the buffer. The value of this parameter must be large enough to hold a <a href="https://msdn.microsoft.com/ec938519-3c0c-4664-9e9a-b7fb338920f5">CLIPLINE</a> structure with at least one <a href="https://msdn.microsoft.com/7c53ec29-2541-40d3-95df-bf73d900a6d6">RUN</a> structure. The driver should allocate space for several RUN structures.


### -param pcl

Pointer to the buffer that receives a CLIPLINE structure. The structure contains the original unclipped control points for a line segment. (The correct pixels for the line cannot be computed without the original points.) RUN structures, which describe sets of pixels along the line that are not clipped away, are written to this buffer.

If a clip region is complex, a single line segment can be broken into many RUN structures. A segment is returned as many times as necessary to list all of its RUN structures.

The CLIPLINE structure contains the starting and ending points of the original unclipped line and the line segments, or RUN structures, of that line that are to appear on the display.


## -returns



The return value is <b>TRUE</b> if more line segments are to be enumerated, indicating that this service should be called again. Otherwise, it is <b>FALSE</b>, indicating that the returned segment is the last segment in the path.




## -remarks



The enumeration must be started with <a href="https://msdn.microsoft.com/3db437aa-40d1-4703-ab1e-b3e154923d2d">PATHOBJ_vEnumStartClipLines</a> before the driver makes this call.




## -see-also




<a href="https://msdn.microsoft.com/ec938519-3c0c-4664-9e9a-b7fb338920f5">CLIPLINE</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/3db437aa-40d1-4703-ab1e-b3e154923d2d">PATHOBJ_vEnumStartClipLines</a>



<a href="https://msdn.microsoft.com/7c53ec29-2541-40d3-95df-bf73d900a6d6">RUN</a>
 

 

