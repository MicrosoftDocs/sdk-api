---
UID: NF:winddi.FLOATOBJ_GreaterThanLong
title: FLOATOBJ_GreaterThanLong function
author: windows-sdk-content
description: The FLOATOBJ_GreaterThanLong function determines whether the FLOATOBJ is greater than the value of type LONG.
old-location: display\floatobj_greaterthanlong.htm
old-project: display
ms.assetid: 2d464472-c89b-47ad-811e-a2f5445e12a9
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: FLOATOBJ_GreaterThanLong, FLOATOBJ_GreaterThanLong function [Display Devices], display.floatobj_greaterthanlong, gdifncs_75edc272-ffac-4ff0-9b3b-c542d3d0ae89.xml, winddi/FLOATOBJ_GreaterThanLong
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
 - FLOATOBJ_GreaterThanLong
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_GreaterThanLong function


## -description


The <b>FLOATOBJ_GreaterThanLong</b> function determines whether the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> is greater than the value of type LONG.


## -parameters




### -param

TBD




#### - l [in]

Specifies the LONG value. This value is converted to a FLOATOBJ for the comparison.


#### - pf [in]

Pointer to the FLOATOBJ.


## -returns



<b>FLOATOBJ_GreaterThanLong </b>returns <b>TRUE</b> if *<i>pf</i> is greater than the FLOATOBJ-equivalent of <i>l</i>; otherwise it returns <b>FALSE</b>.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

