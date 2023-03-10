---
UID: NF:mscat.CryptCATGetMemberInfo
title: CryptCATGetMemberInfo function (mscat.h)
description: Retrieves member information from the catalog's PKCS
helpviewer_keywords: ["CryptCATGetMemberInfo","CryptCATGetMemberInfo function [Security]","mscat/CryptCATGetMemberInfo","security.cryptcatgetmemberinfo"]
old-location: security\cryptcatgetmemberinfo.htm
tech.root: security
ms.assetid: ff265232-f57e-4ab0-ba07-05e6d6745ae3
ms.date: 12/05/2018
ms.keywords: CryptCATGetMemberInfo, CryptCATGetMemberInfo function [Security], mscat/CryptCATGetMemberInfo, security.cryptcatgetmemberinfo
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
 - CryptCATGetMemberInfo
 - mscat/CryptCATGetMemberInfo
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
 - CryptCATGetMemberInfo
---

# CryptCATGetMemberInfo function


## -description

<p class="CCE_Message">[The <b>CryptCATGetMemberInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATGetMemberInfo</b> function retrieves member information from the catalog's PKCS #7. In addition to retrieving the member information for a specified reference tag, this function opens a member context. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatalog [in]

A handle to the catalog. This parameter cannot be <b>NULL</b>.

### -param pwszReferenceTag [in]

A pointer to a <b>null</b>-terminated string that represents the reference tag for the member information being retrieved.

## -returns

A pointer to the [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information or <b>NULL</b>, if no information can be found.

## -remarks

Do not free the returned pointer nor any of the members pointed to by the returned pointer.