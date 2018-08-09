---
UID: NF:winddi.FLOATOBJ_MulFloat
title: FLOATOBJ_MulFloat function
author: windows-sdk-content
description: The FLOATOBJ_MulFloat function multiplies the FLOATOBJ by the value of type FLOATL, and returns with the result in the first parameter.
old-location: display\floatobj_mulfloat.htm
old-project: display
ms.assetid: 7b4189f7-b80b-4543-b713-b0b2d06ef81e
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: FLOATOBJ_MulFloat, FLOATOBJ_MulFloat function [Display Devices], display.floatobj_mulfloat, gdifncs_39da7310-f7d3-4ceb-8bd5-c2a0eaab0068.xml, winddi/FLOATOBJ_MulFloat
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
 - FLOATOBJ_MulFloat
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_MulFloat function


## -description


The <b>FLOATOBJ_MulFloat</b> function multiplies the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> by the value of type FLOATL, and returns with the result in the first parameter.


## -parameters




### -param

TBD




#### - [in, out]

Pointer to the FLOATOBJ operand. When the function returns, *<i>pf</i> will be reset to the value (*<i>pf</i>  *  <i>f</i>).


#### - f [in]

Specifies the FLOATL operand. This value is converted to a FLOATOBJ for the multiplication.


## -returns



None




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

