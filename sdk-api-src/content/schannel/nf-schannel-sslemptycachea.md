---
UID: NF:schannel.SslEmptyCacheA
title: SslEmptyCacheA function
author: windows-sdk-content
description: Removes the specified string from the Schannel cache.
old-location: security\sslemptycache.htm
tech.root: secauthn
ms.assetid: c914d4e3-657e-45ef-ace8-2cea900a8a76
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SslEmptyCache, SslEmptyCache function [Security], SslEmptyCacheA, SslEmptyCacheW, schannel/SslEmptyCache, schannel/SslEmptyCacheA, schannel/SslEmptyCacheW, security.sslemptycache
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SslEmptyCacheA function


## -description


Removes the specified string from the Schannel cache.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Schannel.dll.


## -parameters




### -param pszTargetName [in]

A pointer to a null-terminated string that specifies the entry to remove from the cache. If the value of this parameter is <b>NULL</b>, all entries are removed from the cache.


### -param dwFlags [in]

This parameter is not used.


## -returns



Returns nonzero if the specified entries are removed from the Schannel cache or zero otherwise.



