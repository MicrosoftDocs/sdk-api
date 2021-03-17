---
UID: NF:mscat.CryptCATAdminResolveCatalogPath
title: CryptCATAdminResolveCatalogPath function (mscat.h)
description: Retrieves the fully qualified path of the specified catalog.
helpviewer_keywords: ["CryptCATAdminResolveCatalogPath","CryptCATAdminResolveCatalogPath function [Security]","mscat/CryptCATAdminResolveCatalogPath","security.cryptcatadminresolvecatalogpath"]
old-location: security\cryptcatadminresolvecatalogpath.htm
tech.root: security
ms.assetid: bdbfa02d-8801-40d4-84f4-bc5a449bce50
ms.date: 12/05/2018
ms.keywords: CryptCATAdminResolveCatalogPath, CryptCATAdminResolveCatalogPath function [Security], mscat/CryptCATAdminResolveCatalogPath, security.cryptcatadminresolvecatalogpath
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
req.lib: 
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATAdminResolveCatalogPath
 - mscat/CryptCATAdminResolveCatalogPath
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
 - CryptCATAdminResolveCatalogPath
---

# CryptCATAdminResolveCatalogPath function


## -description

<p class="CCE_Message">[The <b>CryptCATAdminResolveCatalogPath</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminResolveCatalogPath</b> function retrieves the fully qualified path of the specified catalog.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters

### -param hCatAdmin [in]

A handle that was previously assigned by the  <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.

### -param pwszCatalogFile [in]

The name of the catalog file for which to retrieve the fully qualified path.

### -param psCatInfo [in, out]

A pointer to the [CATALOG_INFO](/windows/desktop/api/mscat/ns-mscat-catalog_info) structure. This value cannot be <b>NULL</b>. Upon return from this function, the <i>wszCatalogFile</i> member of the <b>CATALOG_INFO</b> structure contains the catalog file name.

### -param dwFlags [in]

This parameter is reserved and must be set to zero.

## -returns

Returns nonzero if successful or zero otherwise.

For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.