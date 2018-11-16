---
UID: NF:mscat.CryptCATAdminReleaseCatalogContext
title: CryptCATAdminReleaseCatalogContext function
author: windows-sdk-content
description: Releases a handle to a catalog context previously returned by the CryptCATAdminAddCatalog function.
old-location: security\cryptcatadminreleasecatalogcontext.htm
tech.root: SecCrypto
ms.assetid: 6cc13013-2c0a-4934-a866-30b69cbcf934
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CryptCATAdminReleaseCatalogContext, CryptCATAdminReleaseCatalogContext function [Security], mscat/CryptCATAdminReleaseCatalogContext, security.cryptcatadminreleasecatalogcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptCATAdminReleaseCatalogContext
: 
---

# CryptCATAdminReleaseCatalogContext function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminReleaseCatalogContext</b>  function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminReleaseCatalogContext</b> function releases a handle to a catalog context previously returned by the <a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a> function. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle previously assigned by the  <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param hCatInfo [in]

Handle previously assigned by the <a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a> function or the <a href="https://msdn.microsoft.com/33ab2d01-94ab-4d23-a054-9da0731485d6">CryptCATAdminEnumCatalogFromHash</a> function.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>
 

 

