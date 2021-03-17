---
UID: NF:mscat.CryptCATCatalogInfoFromContext
title: CryptCATCatalogInfoFromContext function (mscat.h)
description: Retrieves catalog information from a specified catalog context.
helpviewer_keywords: ["CryptCATCatalogInfoFromContext","CryptCATCatalogInfoFromContext function [Security]","mscat/CryptCATCatalogInfoFromContext","security.cryptcatcataloginfofromcontext"]
old-location: security\cryptcatcataloginfofromcontext.htm
tech.root: security
ms.assetid: ec195fcc-1cff-4dd6-9075-c4904b653da7
ms.date: 12/05/2018
ms.keywords: CryptCATCatalogInfoFromContext, CryptCATCatalogInfoFromContext function [Security], mscat/CryptCATCatalogInfoFromContext, security.cryptcatcataloginfofromcontext
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
 - CryptCATCatalogInfoFromContext
 - mscat/CryptCATCatalogInfoFromContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
 - mscat32.dll
api_name:
 - CryptCATCatalogInfoFromContext
---

# CryptCATCatalogInfoFromContext function


## -description

<p class="CCE_Message">[The <b>CryptCATCatalogInfoFromContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCatalogInfoFromContext</b> function retrieves catalog information from a specified catalog context. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatInfo [in]

A handle to the catalog context. This value cannot be <b>NULL</b>.

### -param psCatInfo [in, out]

A pointer to the [CATALOG_INFO](/windows/desktop/api/mscat/ns-mscat-catalog_info) structure. This value cannot be <b>NULL</b>. Upon return from this function, the <i>wszCatalogFile</i> member of the CATALOG_INFO structure contains the catalog file name.

### -param dwFlags [in]

Unused; set to zero.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.