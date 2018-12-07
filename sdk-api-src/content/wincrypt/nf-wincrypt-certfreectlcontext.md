---
UID: NF:wincrypt.CertFreeCTLContext
title: CertFreeCTLContext function
author: windows-sdk-content
description: Frees a certificate trust list (CTL) context by decrementing its reference count.
old-location: security\certfreectlcontext.htm
tech.root: seccrypto
ms.assetid: 84b1aa0c-44d9-4a2f-861c-fa7d8caac192
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CertFreeCTLContext, CertFreeCTLContext function [Security], _crypto2_certfreectlcontext, security.certfreectlcontext, wincrypt/CertFreeCTLContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFreeCTLContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFreeCTLContext function


## -description


The <b>CertFreeCTLContext</b> function frees a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> by decrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>. When the reference count goes to zero, <b>CertFreeCTLContext</b> frees the memory used by a CTL context.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.


## -parameters




### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> to be freed.


## -returns



The function always returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Trust List Functions</a>
 

 

