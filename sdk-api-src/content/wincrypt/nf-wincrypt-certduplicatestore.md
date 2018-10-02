---
UID: NF:wincrypt.CertDuplicateStore
title: CertDuplicateStore function
author: windows-sdk-content
description: Duplicates a store handle by incrementing the store's reference count.
old-location: security\certduplicatestore.htm
tech.root: seccrypto
ms.assetid: 628efd30-6e07-4748-82ac-5cdc723be451
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CertDuplicateStore, CertDuplicateStore function [Security], _crypto2_certduplicatestore, security.certduplicatestore, wincrypt/CertDuplicateStore
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
 - CertDuplicateStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertDuplicateStore function


## -description


The <b>CertDuplicateStore</b> function duplicates a store handle by incrementing the store's <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>.


## -parameters




### -param hCertStore [in]

A handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> for which the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is being incremented.


## -returns



Currently, a copy is not made of the handle, and the returned handle is the same as the handle that was input. If <b>NULL</b> is passed in, the called function will raise an access violation exception.




## -see-also




<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

