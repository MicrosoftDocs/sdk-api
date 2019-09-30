---
UID: NF:wincrypt.CertDuplicateCTLContext
title: CertDuplicateCTLContext function (wincrypt.h)
author: windows-sdk-content
description: The CertDuplicateCTLContext function duplicates a certificate trust list (CTL) context by incrementing its reference count.
old-location: security\certduplicatectlcontext.htm
tech.root: SecCrypto
ms.assetid: 512d246f-9f22-4ac1-a4fc-d5c615a65cf9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertDuplicateCTLContext, CertDuplicateCTLContext function [Security], _crypto2_certduplicatectlcontext, security.certduplicatectlcontext, wincrypt/CertDuplicateCTLContext
ms.topic: function
f1_keywords:
- wincrypt/CertDuplicateCTLContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertDuplicateCTLContext function


## -description


The <b>CertDuplicateCTLContext</b> function duplicates a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context by incrementing its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a>.


## -parameters




### -param pCtlContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure for which the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a> is being incremented.


## -returns



Currently, a copy is not made of the context, and the returned pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> is the same as pointer input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>
 

 

