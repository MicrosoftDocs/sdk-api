---
UID: NF:mscat.CryptCATAdminEnumCatalogFromHash
title: CryptCATAdminEnumCatalogFromHash function
author: windows-sdk-content
description: Enumerates the catalogs that contain a specified hash.
old-location: security\cryptcatadminenumcatalogfromhash.htm
tech.root: seccrypto
ms.assetid: 33ab2d01-94ab-4d23-a054-9da0731485d6
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CryptCATAdminEnumCatalogFromHash, CryptCATAdminEnumCatalogFromHash function [Security], mscat/CryptCATAdminEnumCatalogFromHash, security.cryptcatadminenumcatalogfromhash
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
 - CryptCATAdminEnumCatalogFromHash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATAdminEnumCatalogFromHash function


## -description


<p class="CCE_Message">[The  <b>CryptCATAdminEnumCatalogFromHash</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminEnumCatalogFromHash</b> function enumerates the catalogs that contain a specified hash. The hash is typically returned from the <a href="https://msdn.microsoft.com/4dc5688f-4b7a-4baf-9671-868cac7f1896">CryptCATAdminCalcHashFromFileHandle</a> function.  This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll. After the final call to this function, call <a href="https://msdn.microsoft.com/6cc13013-2c0a-4934-a866-30b69cbcf934">CryptCATAdminReleaseCatalogContext</a> to release allocated memory.


## -parameters




### -param hCatAdmin [in]

A handle to a catalog administrator context previously assigned by the <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param pbHash [in]

A pointer to the buffer that contains the hash retrieved by calling <a href="https://msdn.microsoft.com/4dc5688f-4b7a-4baf-9671-868cac7f1896">CryptCATAdminCalcHashFromFileHandle</a>.


### -param cbHash [in]

Number of bytes in the buffer allocated for <i>pbHash</i>.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


### -param phPrevCatInfo [in]

A pointer to the handle to the previous catalog context or <b>NULL</b>,  if an enumeration is re-queried. If <b>NULL</b> is passed in for this parameter, then the caller gets information only for the first catalog that contains the hash; an enumeration is not made. If <i>phPrevCatInfo</i> contains <b>NULL</b>, then an enumeration of the catalogs that contain the hash is started, and subsequent calls to <b>CryptCATAdminEnumCatalogFromHash</b> must set <i>phPrevCatInfo</i> to the return value from the previous call.


## -returns



The return value is a handle to the catalog context or <b>NULL</b>,  if there are no more catalogs to enumerate or retrieve.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



