---
UID: NF:mscat.CryptCATAdminResolveCatalogPath
title: CryptCATAdminResolveCatalogPath function
author: windows-sdk-content
description: Retrieves the fully qualified path of the specified catalog.
old-location: security\cryptcatadminresolvecatalogpath.htm
tech.root: seccrypto
ms.assetid: bdbfa02d-8801-40d4-84f4-bc5a449bce50
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CryptCATAdminResolveCatalogPath, CryptCATAdminResolveCatalogPath function [Security], mscat/CryptCATAdminResolveCatalogPath, security.cryptcatadminresolvecatalogpath
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
req.lib: 
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
 - CryptCATAdminResolveCatalogPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATAdminResolveCatalogPath function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminResolveCatalogPath</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminResolveCatalogPath</b> function retrieves the fully qualified path of the specified catalog.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.</div><div> </div>

## -parameters




### -param hCatAdmin [in]

A handle that was previously assigned by the  <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param pwszCatalogFile [in]

The name of the catalog file for which to retrieve the fully qualified path.


### -param psCatInfo [in, out]

A pointer to the <a href="https://msdn.microsoft.com/f6e66412-3ed2-48d9-a377-5df11500db59">CATALOG_INFO</a> structure. This value cannot be <b>NULL</b>. Upon return from this function, the <i>wszCatalogFile</i> member of the <b>CATALOG_INFO</b> structure contains the catalog file name.


### -param dwFlags [in]

This parameter is reserved and must be set to zero.


## -returns



Returns nonzero if successful or zero otherwise.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



