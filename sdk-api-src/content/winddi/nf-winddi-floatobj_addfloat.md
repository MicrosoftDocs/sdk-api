---
UID: NF:winddi.FLOATOBJ_AddFloat
title: FLOATOBJ_AddFloat function
author: windows-driver-content
description: The FLOATOBJ_AddFloat function adds the value of type FLOATL to the FLOATOBJ, and returns with the result in the first parameter.
old-location: display\floatobj_addfloat.htm
old-project: display
ms.assetid: 47af86ec-a7b2-49c1-aeda-1a273f17c4ae
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: FLOATOBJ_AddFloat, FLOATOBJ_AddFloat function [Display Devices], display.floatobj_addfloat, gdifncs_2e5305b6-571f-4ae2-bfd7-2305c006b6da.xml, winddi/FLOATOBJ_AddFloat
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
-	FLOATOBJ_AddFloat
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_AddFloat function


## -description


The <b>FLOATOBJ_AddFloat</b> function adds the value of type FLOATL to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>, and returns with the result in the first parameter.


## -parameters




### -param

TBD




#### - f [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the summation.


#### - pf [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the sum of *<i>pf</i> and *<i>f</i>.


## -returns



None




## -remarks



The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

