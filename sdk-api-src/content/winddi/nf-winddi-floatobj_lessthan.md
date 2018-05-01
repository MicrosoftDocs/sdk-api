---
UID: NF:winddi.FLOATOBJ_LessThan
title: FLOATOBJ_LessThan function
author: windows-driver-content
description: The FLOATOBJ_LessThan function determines whether the first FLOATOBJ is less than the second FLOATOBJ.
old-location: display\floatobj_lessthan.htm
old-project: display
ms.assetid: acd1cc6d-c88f-4336-8a6c-a8b02cf726ee
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FLOATOBJ_LessThan, FLOATOBJ_LessThan function [Display Devices], display.floatobj_lessthan, gdifncs_226d15f4-cebd-45a4-b8e8-7ae7ee770b30.xml, winddi/FLOATOBJ_LessThan
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
-	FLOATOBJ_LessThan
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_LessThan function


## -description


The <b>FLOATOBJ_LessThan</b> function determines whether the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> is less than the second FLOATOBJ.


## -parameters




### -param

TBD




#### - pf [in]

Pointer to the first FLOATOBJ.


#### - pf1 [in]

Pointer to the second FLOATOBJ.


## -returns



<b>FLOATOBJ_LessThan </b>returns <b>TRUE</b> if *<i>pf</i> is less than *<i>pf1</i>; otherwise it returns <b>FALSE</b>.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

