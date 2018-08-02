---
UID: NF:winddi.FLOATOBJ_GreaterThan
title: FLOATOBJ_GreaterThan function
author: windows-sdk-content
description: The FLOATOBJ_GreaterThan function determines whether the first FLOATOBJ is greater than the second FLOATOBJ.
old-location: display\floatobj_greaterthan.htm
old-project: display
ms.assetid: 45e743e4-a72d-413a-9ee3-79eab517c87e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FLOATOBJ_GreaterThan, FLOATOBJ_GreaterThan function [Display Devices], display.floatobj_greaterthan, gdifncs_ac52408a-8df9-4fe2-bf33-35bdfb9fa5d8.xml, winddi/FLOATOBJ_GreaterThan
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FLOATOBJ_GreaterThan
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_GreaterThan function


## -description


The <b>FLOATOBJ_GreaterThan</b> function determines whether the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> is greater than the second FLOATOBJ.


## -parameters




### -param

TBD




#### - pf [in]

Pointer to the first FLOATOBJ.


#### - pf1 [in]

Pointer to the second FLOATOBJ.


## -returns



<b>FLOATOBJ_GreaterThan </b>returns <b>TRUE</b> if *<i>pf</i> is greater than *<i>pf1</i>; otherwise it returns <b>FALSE</b>.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

