---
UID: NF:winddi.FLOATOBJ_Add
title: FLOATOBJ_Add function
author: windows-sdk-content
description: The FLOATOBJ_Add function adds the two FLOATOBJs, and returns with the result in the first parameter.
old-location: display\floatobj_add.htm
tech.root: display
ms.assetid: 6502d863-ab3e-46d2-8da4-c2f1b01fe344
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FLOATOBJ_Add, FLOATOBJ_Add function [Display Devices], display.floatobj_add, gdifncs_484fa853-6c4e-4bc1-95a3-7f7b40828fcc.xml, winddi/FLOATOBJ_Add
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
 - FLOATOBJ_Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_Add function


## -description


The <b>FLOATOBJ_Add</b> function adds the two FLOATOBJs, and returns with the result in the first parameter.


## -parameters




### -param arg1 [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the sum of *<i>pf</i> and *<i>pf1</i>.


### -param arg2 [in]

Pointer to the second FLOATOBJ operand.


## -returns



None




## -remarks



The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

