---
UID: NF:schannel.SslEmptyCacheW
title: SslEmptyCacheW function (schannel.h)
description: Removes the specified string from the Schannel cache.
helpviewer_keywords: ["SslEmptyCache","SslEmptyCache function [Security]","SslEmptyCacheA","SslEmptyCacheW","schannel/SslEmptyCache","schannel/SslEmptyCacheA","schannel/SslEmptyCacheW","security.sslemptycache"]
old-location: security\sslemptycache.htm
tech.root: SecAuthN
ms.assetid: c914d4e3-657e-45ef-ace8-2cea900a8a76
ms.date: 12/05/2018
ms.keywords: SslEmptyCache, SslEmptyCache function [Security], SslEmptyCacheA, SslEmptyCacheW, schannel/SslEmptyCache, schannel/SslEmptyCacheA, schannel/SslEmptyCacheW, security.sslemptycache
f1_keywords:
- schannel/SslEmptyCache
dev_langs:
- c++
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SslEmptyCacheW (Unicode) and SslEmptyCacheA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Schannel.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Schannel.dll
api_name:
- SslEmptyCache
- SslEmptyCacheA
- SslEmptyCacheW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SslEmptyCacheW function


## -description


Removes the specified string from the Schannel cache.

This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Schannel.dll.


## -parameters




### -param pszTargetName [in]

A pointer to a null-terminated string that specifies the entry to remove from the cache. If the value of this parameter is <b>NULL</b>, all entries are removed from the cache.


### -param dwFlags [in]

This parameter is not used.


## -returns



Returns nonzero if the specified entries are removed from the Schannel cache or zero otherwise.



