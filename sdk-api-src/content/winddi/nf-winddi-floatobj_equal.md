---
UID: NF:winddi.FLOATOBJ_Equal
title: FLOATOBJ_Equal function
author: windows-sdk-content
description: The FLOATOBJ_Equal function determines whether the two FLOATOBJs are equal.
old-location: display\floatobj_equal.htm
old-project: display
ms.assetid: 1fc9afcb-7b65-415c-ae6c-8885ef47abe9
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: FLOATOBJ_Equal, FLOATOBJ_Equal function [Display Devices], display.floatobj_equal, gdifncs_20ba1db5-2709-4765-a637-94000c803ecb.xml, winddi/FLOATOBJ_Equal
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	FLOATOBJ_Equal
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FLOATOBJ_Equal function


## -description


The <b>FLOATOBJ_Equal</b> function determines whether the two <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>s are equal.


## -parameters




### -param

TBD




#### - pf [in]

Pointer to the first FLOATOBJ operand.


#### - pf1 [in]

Pointer to the second FLOATOBJ operand.


## -returns



<b>FLOATOBJ_Equal </b>returns <b>TRUE</b> if *<i>pf</i> and *<i>pf1</i> are equal; otherwise it returns <b>FALSE</b>.




## -remarks



The <b>FLOATOBJ_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

