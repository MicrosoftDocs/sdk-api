---
UID: NF:winddi.FLOATOBJ_Neg
title: FLOATOBJ_Neg function
author: windows-driver-content
description: The FLOATOBJ_Neg function negates the FLOATOBJ.
old-location: display\floatobj_neg.htm
old-project: display
ms.assetid: 08a4c47f-8bf5-4849-8ce9-e5999c02f263
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FLOATOBJ_Neg, FLOATOBJ_Neg function [Display Devices], display.floatobj_neg, gdifncs_7fe9b86a-abdd-44d6-b815-1ac5f37203db.xml, winddi/FLOATOBJ_Neg
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
-	FLOATOBJ_Neg
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_Neg function


## -description


The <b>FLOATOBJ_Neg</b> function negates the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>.


## -parameters




### -param Arg1

TBD




#### - pf [in, out]

Pointer to the FLOATOBJ to be negated. When the function returns, *<i>pf</i> will contain the negated value.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

