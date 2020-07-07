---
UID: NF:mscat.CryptCATClose
title: CryptCATClose function (mscat.h)
description: Closes a catalog handle opened previously by the CryptCATOpen function.
helpviewer_keywords: ["CryptCATClose","CryptCATClose function [Security]","mscat/CryptCATClose","security.cryptcatclose"]
old-location: security\cryptcatclose.htm
tech.root: SecCrypto
ms.assetid: f6fa2d10-0049-4d5e-9688-566e5c11d64e
ms.date: 12/05/2018
ms.keywords: CryptCATClose, CryptCATClose function [Security], mscat/CryptCATClose, security.cryptcatclose
f1_keywords:
- mscat/CryptCATClose
dev_langs:
- c++
req.header: mscat.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wintrust.dll
api_name:
- CryptCATClose
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptCATClose function


## -description


<p class="CCE_Message">[The <b>CryptCATClose</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATClose</b> function closes a catalog handle opened previously by the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function. This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatalog [in]

Handle opened previously by a call to the  <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a>
 

 

