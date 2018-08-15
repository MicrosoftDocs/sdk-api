---
UID: NF:winddi.FLOATOBJ_GetFloat
title: FLOATOBJ_GetFloat function
author: windows-sdk-content
description: The FLOATOBJ_GetFloat function calculates and returns the FLOAT-equivalent value of the specified FLOATOBJ.
old-location: display\floatobj_getfloat.htm
old-project: display
ms.assetid: 1deddee5-c987-45b0-bb0f-ff4f766fdde0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: FLOATOBJ_GetFloat, FLOATOBJ_GetFloat function [Display Devices], display.floatobj_getfloat, gdifncs_6f6c6936-a1f3-41d0-835d-52abc1140cc2.xml, winddi/FLOATOBJ_GetFloat
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
 - FLOATOBJ_GetFloat
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_GetFloat function


## -description


The <b>FLOATOBJ_GetFloat</b> function calculates and returns the FLOAT-equivalent value of the specified <a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>.


## -parameters




### -param Arg1 [in]

Pointer to the FLOATOBJ to be converted to a FLOAT.


## -returns



<b>FLOATOBJ_GetFloat</b> returns the FLOAT-equivalent value of *<i>pf</i>. The return value is of type LONG, and needs to be typecast to a FLOAT by the driver.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/5f8c401b-7487-4d75-a0a8-534fa7992a3d">FLOATOBJ</a>
 

 

