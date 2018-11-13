---
UID: NF:wincrypt.CertDuplicateCTLContext
title: CertDuplicateCTLContext function
author: windows-sdk-content
description: The CertDuplicateCTLContext function duplicates a certificate trust list (CTL) context by incrementing its reference count.
old-location: security\certduplicatectlcontext.htm
tech.root: seccrypto
ms.assetid: 512d246f-9f22-4ac1-a4fc-d5c615a65cf9
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertDuplicateCTLContext, CertDuplicateCTLContext function [Security], _crypto2_certduplicatectlcontext, security.certduplicatectlcontext, wincrypt/CertDuplicateCTLContext
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
 - CertDuplicateCTLContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertDuplicateCTLContext function


## -description


The <b>CertDuplicateCTLContext</b> function duplicates a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context by incrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>.


## -parameters




### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure for which the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is being incremented.


## -returns



Currently, a copy is not made of the context, and the returned pointer to <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> is the same as pointer input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned.




## -see-also




<a href="cryptography_functions.htm">Certificate Trust List Functions</a>
 

 

