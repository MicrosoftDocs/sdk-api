---
UID: NF:winddi.FLOATOBJ_SubLong
title: FLOATOBJ_SubLong function
author: windows-sdk-content
description: The FLOATOBJ_SubLong function subtracts the value of type LONG from the FLOATOBJ, and returns with the result in the first parameter.
old-location: display\floatobj_sublong.htm
old-project: display
ms.assetid: 2a3e8a17-3718-4212-adfe-f109e286bec6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: FLOATOBJ_SubLong, FLOATOBJ_SubLong function [Display Devices], display.floatobj_sublong, gdifncs_8b50c7a1-6ed7-4368-8465-5b1b1e7f4c48.xml, winddi/FLOATOBJ_SubLong
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
 - FLOATOBJ_SubLong
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_SubLong function


## -description


The <b>FLOATOBJ_SubLong</b> function subtracts the value of type LONG from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>, and returns with the result in the first parameter.


## -parameters




### -param

TBD




#### - [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i> - <i>l</i>).


#### - l [in]

Specifies the LONG operand. This value is converted to a FLOATOBJ for the subtraction.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

