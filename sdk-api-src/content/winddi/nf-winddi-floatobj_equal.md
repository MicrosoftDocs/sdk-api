---
UID: NF:winddi.FLOATOBJ_Equal
title: FLOATOBJ_Equal function (winddi.h)
author: windows-sdk-content
description: The FLOATOBJ_Equal function determines whether the two FLOATOBJs are equal.
old-location: display\floatobj_equal.htm
tech.root: display
ms.assetid: 1fc9afcb-7b65-415c-ae6c-8885ef47abe9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_Equal, FLOATOBJ_Equal function [Display Devices], display.floatobj_equal, gdifncs_20ba1db5-2709-4765-a637-94000c803ecb.xml, winddi/FLOATOBJ_Equal
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
 - FLOATOBJ_Equal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FLOATOBJ_Equal function


## -description


The <b>FLOATOBJ_Equal</b> function determines whether the two <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>s are equal.


## -parameters




### -param arg1 [in]

Pointer to the first FLOATOBJ operand.


### -param arg2 [in]

Pointer to the second FLOATOBJ operand.


## -returns



<b>FLOATOBJ_Equal </b>returns <b>TRUE</b> if *<i>pf</i> and *<i>pf1</i> are equal; otherwise it returns <b>FALSE</b>.




## -remarks



The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

