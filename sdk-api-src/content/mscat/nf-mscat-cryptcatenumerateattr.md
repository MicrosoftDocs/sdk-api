---
UID: NF:mscat.CryptCATEnumerateAttr
title: CryptCATEnumerateAttr function (mscat.h)
description: Enumerates the attributes associated with a member of a catalog. This function has no associated import library.
helpviewer_keywords: ["CryptCATEnumerateAttr","CryptCATEnumerateAttr function [Security]","mscat/CryptCATEnumerateAttr","security.cryptcatenumerateattr"]
old-location: security\cryptcatenumerateattr.htm
tech.root: security
ms.assetid: 064e87db-4330-4b8b-9865-ba8b9714f6e4
ms.date: 12/05/2018
ms.keywords: CryptCATEnumerateAttr, CryptCATEnumerateAttr function [Security], mscat/CryptCATEnumerateAttr, security.cryptcatenumerateattr
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
 - CryptCATEnumerateAttr
 - mscat/CryptCATEnumerateAttr
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
 - CryptCATEnumerateAttr
---

# CryptCATEnumerateAttr function


## -description

<p class="CCE_Message">[The <b>CryptCATEnumerateAttr</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateAttr</b> function enumerates the attributes associated with  a member of a catalog. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatalog [in]

Handle for the catalog that contains the member identified by <i>pCatMember</i>. This value cannot be <b>NULL</b>.

### -param pCatMember [in]

A pointer to the [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that identifies which member of the catalog is being enumerated.

### -param pPrevAttr [in]

A pointer to the previously returned value from this function or pointer to <b>NULL</b> to start the enumeration.

## -returns

The return value is a pointer to the  CRYPTCATATTRIBUTE structure that contains the attribute information or <b>NULL</b>, if no more attributes are in the enumeration or if an error is encountered. The returned pointer is passed in as the <i>pPrevAttr</i> parameter for subsequent calls to this function.

## -remarks

Do not free the returned pointer nor any of the members pointed to by the returned pointer.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatenumeratecatattr">CryptCATEnumerateCatAttr</a>