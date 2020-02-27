---
UID: NF:mscat.CryptCATAdminReleaseCatalogContext
title: CryptCATAdminReleaseCatalogContext function (mscat.h)
description: Releases a handle to a catalog context previously returned by the CryptCATAdminAddCatalog function.
old-location: security\cryptcatadminreleasecatalogcontext.htm
tech.root: SecCrypto
ms.assetid: 6cc13013-2c0a-4934-a866-30b69cbcf934
ms.date: 12/05/2018
ms.keywords: CryptCATAdminReleaseCatalogContext, CryptCATAdminReleaseCatalogContext function [Security], mscat/CryptCATAdminReleaseCatalogContext, security.cryptcatadminreleasecatalogcontext
f1_keywords:
- mscat/CryptCATAdminReleaseCatalogContext
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
- CryptCATAdminReleaseCatalogContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptCATAdminReleaseCatalogContext function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminReleaseCatalogContext</b>  function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminReleaseCatalogContext</b> function releases a handle to a catalog context previously returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a> function. This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle previously assigned by the  <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext">CryptCATAdminAcquireContext</a> function.


### -param hCatInfo [in]

Handle previously assigned by the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a> function or the <a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminenumcatalogfromhash">CryptCATAdminEnumCatalogFromHash</a> function.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>
 

 

