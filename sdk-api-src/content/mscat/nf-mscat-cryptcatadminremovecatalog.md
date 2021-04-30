---
UID: NF:mscat.CryptCATAdminRemoveCatalog
title: CryptCATAdminRemoveCatalog function (mscat.h)
description: Deletes a catalog file and removes that catalog's entry from the Windows catalog database.
helpviewer_keywords: ["CryptCATAdminRemoveCatalog","CryptCATAdminRemoveCatalog function [Security]","mscat/CryptCATAdminRemoveCatalog","security.cryptcatadminremovecatalog"]
old-location: security\cryptcatadminremovecatalog.htm
tech.root: security
ms.assetid: e09fe991-0e7a-45da-910a-8cb148bdff9a
ms.date: 12/05/2018
ms.keywords: CryptCATAdminRemoveCatalog, CryptCATAdminRemoveCatalog function [Security], mscat/CryptCATAdminRemoveCatalog, security.cryptcatadminremovecatalog
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
 - CryptCATAdminRemoveCatalog
 - mscat/CryptCATAdminRemoveCatalog
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
 - CryptCATAdminRemoveCatalog
---

# CryptCATAdminRemoveCatalog function


## -description

<p class="CCE_Message">[The <b>CryptCATAdminRemoveCatalog</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminRemoveCatalog</b> function deletes a catalog file and removes that catalog's entry from the Windows catalog database. This function is the only supported way to remove catalogs from the database while ensuring the integrity of the database. The function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatAdmin [in]

Handle previously assigned by the  <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.

### -param pwszCatalogFile [in]

A pointer to a null-terminated string for the name of the catalog to remove. This string must contain only the name, without any path information.

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>