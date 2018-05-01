---
UID: NF:winddi.FLOATOBJ_AddLong
title: FLOATOBJ_AddLong function
author: windows-driver-content
description: The FLOATOBJ_AddLong function adds the value of type LONG to the FLOATOBJ, and returns with the result in the first parameter.
old-location: display\floatobj_addlong.htm
old-project: display
ms.assetid: a6355e47-5373-4b03-bafc-308a64e8e0aa
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FLOATOBJ_AddLong, FLOATOBJ_AddLong function [Display Devices], display.floatobj_addlong, gdifncs_d669d0ec-1d1e-4e14-b259-cd7b8bfe5d85.xml, winddi/FLOATOBJ_AddLong
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	FLOATOBJ_AddLong
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_AddLong function


## -description


The <b>FLOATOBJ_AddLong</b> function adds the value of type LONG to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>, and returns with the result in the first parameter.


## -parameters




### -param

TBD




#### - l [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the summation.


#### - pf [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the sum of *<i>pf</i> and *<i>f</i>.


## -returns



None




## -remarks



The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

