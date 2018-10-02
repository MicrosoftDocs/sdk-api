---
UID: NF:winddi.FLOATOBJ_SubLong
title: FLOATOBJ_SubLong function
author: windows-sdk-content
description: The FLOATOBJ_SubLong function subtracts the value of type LONG from the FLOATOBJ, and returns with the result in the first parameter.
old-location: display\floatobj_sublong.htm
tech.root: Display
ms.assetid: 2a3e8a17-3718-4212-adfe-f109e286bec6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FLOATOBJ_SubLong, FLOATOBJ_SubLong function [Display Devices], display.floatobj_sublong, gdifncs_8b50c7a1-6ed7-4368-8465-5b1b1e7f4c48.xml, winddi/FLOATOBJ_SubLong
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
 - FLOATOBJ_SubLong
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_SubLong function


## -description


The <b>FLOATOBJ_SubLong</b> function subtracts the value of type LONG from the <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>, and returns with the result in the first parameter.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i> - <i>l</i>).


#### - l [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the subtraction.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

