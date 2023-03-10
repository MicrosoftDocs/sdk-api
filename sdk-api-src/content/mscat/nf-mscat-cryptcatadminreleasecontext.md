---
UID: NF:mscat.CryptCATAdminReleaseContext
title: CryptCATAdminReleaseContext function (mscat.h)
description: Releases the handle previously assigned by the CryptCATAdminAcquireContext function.
helpviewer_keywords: ["CryptCATAdminReleaseContext","CryptCATAdminReleaseContext function [Security]","mscat/CryptCATAdminReleaseContext","security.cryptcatadminreleasecontext"]
old-location: security\cryptcatadminreleasecontext.htm
tech.root: security
ms.assetid: dff253dc-c444-46be-a383-41340d634cce
ms.date: 12/05/2018
ms.keywords: CryptCATAdminReleaseContext, CryptCATAdminReleaseContext function [Security], mscat/CryptCATAdminReleaseContext, security.cryptcatadminreleasecontext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATAdminReleaseContext
 - mscat/CryptCATAdminReleaseContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminReleaseContext
---

# CryptCATAdminReleaseContext function


## -description

<p class="CCE_Message">[The  <b>CryptCATAdminReleaseContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminReleaseContext</b> function releases the handle previously assigned by the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatAdmin [in]

Catalog administrator context handle previously  assigned by a call to the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.

### -param dwFlags [in]

Not used; set to  zero.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a>