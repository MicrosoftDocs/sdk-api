---
UID: NF:mscat.CryptCATAdminAcquireContext
title: CryptCATAdminAcquireContext function (mscat.h)
description: Acquires a handle to a catalog administrator context.helpviewer_keywords: ["CryptCATAdminAcquireContext","CryptCATAdminAcquireContext function [Security]","mscat/CryptCATAdminAcquireContext","security.cryptcatadminacquirecontext"]
old-location: security\cryptcatadminacquirecontext.htm
tech.root: SecCrypto
ms.assetid: 693af055-fa93-4526-aa9c-3a659f8ff78f
ms.date: 12/05/2018
ms.keywords: CryptCATAdminAcquireContext, CryptCATAdminAcquireContext function [Security], mscat/CryptCATAdminAcquireContext, security.cryptcatadminacquirecontext
f1_keywords:
- mscat/CryptCATAdminAcquireContext
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
- CryptCATAdminAcquireContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptCATAdminAcquireContext function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminAcquireContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminAcquireContext</b> function acquires a handle to a catalog administrator context. This handle can be used by subsequent calls to the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>,  <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminenumcatalogfromhash">CryptCATAdminEnumCatalogFromHash</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminremovecatalog">CryptCATAdminRemoveCatalog</a> functions. This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param phCatAdmin [out]

A pointer to the catalog administrator context handle that is assigned by this function. When you have finished using the handle, close it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecontext">CryptCATAdminReleaseContext</a> function.


### -param pgSubsystem [in]

A pointer to the GUID that identifies the subsystem. DRIVER_ACTION_VERIFY represents the subsystem for operating system components and third party drivers. This is the subsystem used by most implementations.


### -param dwFlags [in]

Not used; set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecontext">CryptCATAdminReleaseContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminremovecatalog">CryptCATAdminRemoveCatalog</a>
 

 

