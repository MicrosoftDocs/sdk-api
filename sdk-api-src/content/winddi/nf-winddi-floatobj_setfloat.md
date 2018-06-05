---
UID: NF:winddi.FLOATOBJ_SetFloat
title: FLOATOBJ_SetFloat function
author: windows-sdk-content
description: The FLOATOBJ_SetFloat function assigns the value of type FLOATL to the FLOATOBJ.
old-location: display\floatobj_setfloat.htm
old-project: display
ms.assetid: ba2c33fa-9489-482d-b27e-79537425cc4b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: FLOATOBJ_SetFloat, FLOATOBJ_SetFloat function [Display Devices], display.floatobj_setfloat, gdifncs_3bf0c118-feea-48f1-8e20-d3b43408a860.xml, winddi/FLOATOBJ_SetFloat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	FLOATOBJ_SetFloat
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_SetFloat function


## -description


The <b>FLOATOBJ_SetFloat</b> function assigns the value of type FLOATL to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>.


## -parameters




### -param

TBD




#### - f [in]

Specifies the FLOATL value. This value is converted to a FLOATOBJ for the assignment.


#### - pf [out]

Pointer to the FLOATOBJ that will receive the value of <i>f</i>.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

