---
UID: NF:mscat.CryptCATEnumerateCatAttr
title: CryptCATEnumerateCatAttr function (mscat.h)
description: Enumerates the attributes associated with a catalog. This function has no associated import library.
helpviewer_keywords: ["CryptCATEnumerateCatAttr","CryptCATEnumerateCatAttr function [Security]","mscat/CryptCATEnumerateCatAttr","security.cryptcatenumeratecatattr"]
old-location: security\cryptcatenumeratecatattr.htm
tech.root: security
ms.assetid: 57b6ff5c-e47e-41ac-8ec8-01a47ea77acf
ms.date: 12/05/2018
ms.keywords: CryptCATEnumerateCatAttr, CryptCATEnumerateCatAttr function [Security], mscat/CryptCATEnumerateCatAttr, security.cryptcatenumeratecatattr
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
 - CryptCATEnumerateCatAttr
 - mscat/CryptCATEnumerateCatAttr
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
 - CryptCATEnumerateCatAttr
---

# CryptCATEnumerateCatAttr function


## -description

<p class="CCE_Message">[The <b>CryptCATEnumerateCatAttr</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateCatAttr</b> function enumerates the attributes associated with  a catalog. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatalog [in]

Handle for the catalog whose attributes are being enumerated. This value cannot be <b>NULL</b>.

### -param pPrevAttr [in]

A pointer to the previously returned pointer to  the [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure from this function or pointer to <b>NULL</b> to start the enumeration.

## -returns

The return value is a pointer to the  [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure that contains the attribute information or <b>NULL</b>, if no more attributes are in the enumeration or if an error is encountered. The returned pointer is passed in as the <i>pPrevAttr</i> parameter for subsequent calls to this function.

## -remarks

Do not free the returned pointer nor any of the members pointed to by the returned pointer.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatenumerateattr">CryptCATEnumerateAttr</a>