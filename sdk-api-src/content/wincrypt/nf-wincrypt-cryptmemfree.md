---
UID: NF:wincrypt.CryptMemFree
title: CryptMemFree function
author: windows-sdk-content
description: The CryptMemFree function frees memory allocated by CryptMemAlloc or CryptMemRealloc.
old-location: security\cryptmemfree.htm
old-project: SecCrypto
ms.assetid: fb5c10ba-da8e-4a34-9302-67586a0a9624
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CryptMemFree, CryptMemFree function [Security], _crypto2_cryptmemfree, security.cryptmemfree, wincrypt/CryptMemFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptMemFree
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMemFree function


## -description


The <b>CryptMemFree</b> function frees memory allocated by 
<a href="https://msdn.microsoft.com/ac7588b1-ff8c-4f8d-a8ab-f0e8a18e5614">CryptMemAlloc</a> or 
<a href="https://msdn.microsoft.com/74bdd2dd-9f05-4d36-8323-79d547820068">CryptMemRealloc</a>.


## -parameters




### -param pv [in]

A pointer to the buffer to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/ac7588b1-ff8c-4f8d-a8ab-f0e8a18e5614">CryptMemAlloc</a>



<a href="https://msdn.microsoft.com/74bdd2dd-9f05-4d36-8323-79d547820068">CryptMemRealloc</a>
 

 

