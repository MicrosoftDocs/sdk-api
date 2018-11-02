---
UID: NF:winddi.FLOATOBJ_Sub
title: FLOATOBJ_Sub function
author: windows-sdk-content
description: The FLOATOBJ_Sub function subtracts the second FLOATOBJ from the first, and returns with the result in the first parameter.
old-location: display\floatobj_sub.htm
tech.root: display
ms.assetid: 0ba6edfa-2de6-4eaa-8853-0e20c01cedf8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FLOATOBJ_Sub, FLOATOBJ_Sub function [Display Devices], display.floatobj_sub, gdifncs_b1e31de5-5ada-4dc0-9946-a758cae47594.xml, winddi/FLOATOBJ_Sub
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
 - FLOATOBJ_Sub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_Sub function


## -description


The <b>FLOATOBJ_Sub</b> function subtracts the second <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a> from the first, and returns with the result in the first parameter.


## -parameters




### -param arg1 [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i> - *<i>pf1</i>).


### -param arg2 [in]

Pointer to the second FLOATOBJ operand.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

