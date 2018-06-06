---
UID: NF:winddi.EngMulDiv
title: EngMulDiv function
author: windows-sdk-content
description: The EngMulDiv function multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value.
old-location: display\engmuldiv.htm
old-project: display
ms.assetid: e1d9d790-4038-445c-a1ea-fe689cb0e694
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngMulDiv, EngMulDiv function [Display Devices], display.engmuldiv, gdifncs_0d175bf5-b421-43e5-acc5-a11299b0d990.xml, winddi/EngMulDiv
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
 - EngMulDiv
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngMulDiv function


## -description


The <b>EngMulDiv</b> function multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value. 


## -parameters




### -param a [in]

Specifies the 32-bit signed multiplicand.


### -param b [in]

Specifies the 32-bit signed multiplier.


### -param c [in]

Specifies the 32-bit signed divisor by which the result of <i>a</i>*<i>b</i> is to be divided.


## -returns



<b>EngMulDiv</b> returns the signed 32-bit result of the multiplication and division. The return value is rounded up or down to the nearest integer.




## -remarks



Drivers should not pass a zero divisor to <b>EngMulDiv</b>.



