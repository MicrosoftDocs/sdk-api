---
UID: NF:mscat.CryptCATAdminEnumCatalogFromHash
title: CryptCATAdminEnumCatalogFromHash function (mscat.h)
author: windows-sdk-content
description: Enumerates the catalogs that contain a specified hash.
old-location: security\cryptcatadminenumcatalogfromhash.htm
tech.root: SecCrypto
ms.assetid: 33ab2d01-94ab-4d23-a054-9da0731485d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptCATAdminEnumCatalogFromHash, CryptCATAdminEnumCatalogFromHash function [Security], mscat/CryptCATAdminEnumCatalogFromHash, security.cryptcatadminenumcatalogfromhash
ms.topic: function
f1_keywords: 
 - "mscat/CryptCATAdminEnumCatalogFromHash"
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
 - mscat32.dll
api_name:
 - CryptCATAdminEnumCatalogFromHash
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptCATAdminEnumCatalogFromHash function


## -description


<p class="CCE_Message">[The  <b>CryptCATAdminEnumCatalogFromHash</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminEnumCatalogFromHash</b> function enumerates the catalogs that contain a specified hash. The hash is typically returned from the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle">CryptCATAdminCalcHashFromFileHandle</a> function.  This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll. After the final call to this function, call <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecatalogcontext">CryptCATAdminReleaseCatalogContext</a> to release allocated memory.


## -parameters




### -param hCatAdmin [in]

A handle to a catalog administrator context previously assigned by the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.


### -param pbHash [in]

A pointer to the buffer that contains the hash retrieved by calling <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle">CryptCATAdminCalcHashFromFileHandle</a>.


### -param cbHash [in]

Number of bytes in the buffer allocated for <i>pbHash</i>.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


### -param phPrevCatInfo [in]

A pointer to the handle to the previous catalog context or <b>NULL</b>,  if an enumeration is re-queried. If <b>NULL</b> is passed in for this parameter, then the caller gets information only for the first catalog that contains the hash; an enumeration is not made. If <i>phPrevCatInfo</i> contains <b>NULL</b>, then an enumeration of the catalogs that contain the hash is started, and subsequent calls to <b>CryptCATAdminEnumCatalogFromHash</b> must set <i>phPrevCatInfo</i> to the return value from the previous call.


## -returns



The return value is a handle to the catalog context or <b>NULL</b>,  if there are no more catalogs to enumerate or retrieve.

For extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.



