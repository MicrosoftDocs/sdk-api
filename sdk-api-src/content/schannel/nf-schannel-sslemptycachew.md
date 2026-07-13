---
UID: NF:schannel.SslEmptyCacheW
title: SslEmptyCacheW function (schannel.h)
description: Removes the specified string from the Schannel cache. (Unicode)
helpviewer_keywords: ["SslEmptyCache", "SslEmptyCache function [Security]", "SslEmptyCacheW", "schannel/SslEmptyCache", "schannel/SslEmptyCacheW", "security.sslemptycache"]
old-location: security\sslemptycache.htm
tech.root: security
ms.assetid: c914d4e3-657e-45ef-ace8-2cea900a8a76
ms.date: 12/05/2018
ms.keywords: SslEmptyCache, SslEmptyCache function [Security], SslEmptyCacheA, SslEmptyCacheW, schannel/SslEmptyCache, schannel/SslEmptyCacheA, schannel/SslEmptyCacheW, security.sslemptycache
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SslEmptyCacheW
 - schannel/SslEmptyCacheW
dev_langs:
 - c++
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
---

# SslEmptyCacheW function


## -description

Removes the specified string from the Schannel cache.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Schannel.dll.

## -parameters

### -param pszTargetName [in]

A pointer to a null-terminated string that specifies the entry to remove from the cache. If the value of this parameter is <b>NULL</b>, all entries are removed from the cache.

### -param dwFlags [in]

This parameter is not used.

## -returns

Returns nonzero if the specified entries are removed from the Schannel cache or zero otherwise.

## -remarks

> [!NOTE]
> The schannel.h header defines SslEmptyCache as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
