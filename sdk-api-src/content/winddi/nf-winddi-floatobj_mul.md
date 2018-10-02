---
UID: NF:winddi.FLOATOBJ_Mul
title: FLOATOBJ_Mul function
author: windows-sdk-content
description: The FLOATOBJ_Mul function multiplies the two FLOATOBJs, and returns with the result in the first parameter.
old-location: display\floatobj_mul.htm
tech.root: Display
ms.assetid: 95b4c3eb-5e62-4209-9c05-eae9ab48f7ab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FLOATOBJ_Mul, FLOATOBJ_Mul function [Display Devices], display.floatobj_mul, gdifncs_1647a791-7781-4e67-a7b1-06b283c32b0b.xml, winddi/FLOATOBJ_Mul
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
 - FLOATOBJ_Mul
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_Mul function


## -description


The <b>FLOATOBJ_Mul</b> function multiplies the two <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>s, and returns with the result in the first parameter.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - [in, out]

Pointer to the first FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value ( *<i>pf</i>  *  *<i>pf1</i>).


#### - pf1 [in]

Pointer to the second FLOATOBJ operand.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

