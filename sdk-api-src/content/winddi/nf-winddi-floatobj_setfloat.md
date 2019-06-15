---
UID: NF:winddi.FLOATOBJ_SetFloat
title: FLOATOBJ_SetFloat function (winddi.h)
author: windows-sdk-content
description: The FLOATOBJ_SetFloat function assigns the value of type FLOATL to the FLOATOBJ.
old-location: display\floatobj_setfloat.htm
tech.root: display
ms.assetid: ba2c33fa-9489-482d-b27e-79537425cc4b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FLOATOBJ_SetFloat, FLOATOBJ_SetFloat function [Display Devices], display.floatobj_setfloat, gdifncs_3bf0c118-feea-48f1-8e20-d3b43408a860.xml, winddi/FLOATOBJ_SetFloat
ms.topic: function
f1_keywords: ["winddi/FLOATOBJ_SetFloat"]
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
 - FLOATOBJ_SetFloat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FLOATOBJ_SetFloat function


## -description


The <b>FLOATOBJ_SetFloat</b> function assigns the value of type FLOATL to the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_floatobj">FLOATOBJ</a>.


## -parameters




### -param arg1 [out]

Pointer to the FLOATOBJ that will receive the value of <i>f</i>.


### -param arg2 [in]

Specifies the FLOATL value. This value is converted to a FLOATOBJ for the assignment.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_floatobj">FLOATOBJ</a>
 

 

