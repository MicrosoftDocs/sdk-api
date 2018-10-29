---
UID: NF:winddi.FLOATOBJ_SetLong
title: FLOATOBJ_SetLong function
author: windows-sdk-content
description: The FLOATOBJ_SetLong function assigns the value of type LONG to the FLOATOBJ.
old-location: display\floatobj_setlong.htm
tech.root: display
ms.assetid: 4fa1b8a6-8172-4047-9ee2-fe00f0924487
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FLOATOBJ_SetLong, FLOATOBJ_SetLong function [Display Devices], display.floatobj_setlong, gdifncs_b0a076a3-766b-42fb-a04d-5da69177656b.xml, winddi/FLOATOBJ_SetLong
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
 - FLOATOBJ_SetLong
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_SetLong function


## -description


The <b>FLOATOBJ_SetLong</b> function assigns the value of type LONG to the <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>.


## -parameters




### -param arg1 [out]

Pointer to the FLOATOBJ that will receive the value of <i>l</i>.


### -param arg2 [in]

Specifies the LONG value. This value is converted to a FLOATOBJ for the assignment.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

