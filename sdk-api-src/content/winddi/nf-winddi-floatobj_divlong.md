---
UID: NF:winddi.FLOATOBJ_DivLong
title: FLOATOBJ_DivLong function
author: windows-driver-content
description: The FLOATOBJ_DivLong function divides the FLOATOBJ by the value of type LONG, and returns with the result in the first parameter.
old-location: display\floatobj_divlong.htm
old-project: display
ms.assetid: 23452749-1a10-4d19-b24a-24ec42931efd
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: FLOATOBJ_DivLong, FLOATOBJ_DivLong function [Display Devices], display.floatobj_divlong, gdifncs_2c12858b-3c1a-4f4e-883f-aa4527695961.xml, winddi/FLOATOBJ_DivLong
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
-	FLOATOBJ_DivLong
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_DivLong function


## -description


The <b>FLOATOBJ_DivLong</b> function divides the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> by the value of type LONG, and returns with the result in the first parameter.


## -parameters




### -param

TBD




#### - l [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the division.


#### - pf [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the quotient of *<i>pf</i> divided by <i>l</i>.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

