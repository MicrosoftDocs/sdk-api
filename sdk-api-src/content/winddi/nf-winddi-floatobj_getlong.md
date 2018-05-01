---
UID: NF:winddi.FLOATOBJ_GetLong
title: FLOATOBJ_GetLong function
author: windows-driver-content
description: The FLOATOBJ_GetLong function calculates and returns the LONG-equivalent value of the specified FLOATOBJ.
old-location: display\floatobj_getlong.htm
old-project: display
ms.assetid: e3f4355f-c716-4757-9f82-d4f109e05845
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: FLOATOBJ_GetLong, FLOATOBJ_GetLong function [Display Devices], display.floatobj_getlong, gdifncs_bed59b75-53b6-4f6c-975f-a927c5855f2a.xml, winddi/FLOATOBJ_GetLong
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
-	FLOATOBJ_GetLong
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_GetLong function


## -description


The <b>FLOATOBJ_GetLong</b> function calculates and returns the LONG-equivalent value of the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>.


## -parameters




### -param Arg1

TBD




#### - pf [in]

Pointer to the FLOATOBJ to be converted to a LONG.


## -returns



<b>FLOATOBJ_GetFloat</b> returns the LONG-equivalent value of *<i>pf</i>.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

