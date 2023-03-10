---
UID: NF:davclnt.DavInvalidateCache
title: DavInvalidateCache function (davclnt.h)
description: Invalidates the contents of the local cache for a remote file on a WebDAV server.
helpviewer_keywords: ["DavInvalidateCache","DavInvalidateCache function [WebDAV]","davclnt/DavInvalidateCache","webdav.davinvalidatecache"]
old-location: webdav\davinvalidatecache.htm
tech.root: WebDAV
ms.assetid: f111b19c-5472-463a-b33d-7d2188d224e8
ms.date: 12/05/2018
ms.keywords: DavInvalidateCache, DavInvalidateCache function [WebDAV], davclnt/DavInvalidateCache, webdav.davinvalidatecache
req.header: davclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Davclnt.lib
req.dll: Davclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DavInvalidateCache
 - davclnt/DavInvalidateCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - davclnt.dll
api_name:
 - DavInvalidateCache
---

# DavInvalidateCache function


## -description

Invalidates the contents of the local cache for a remote file on a WebDAV server.

## -parameters

### -param URLName [in]

A pointer to a Unicode string that contains the name of a remote file on a WebDAV server. This name can be an HTTP path name (URL) or a UNC path name.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The  <b>DavInvalidateCache</b> function marks the contents of the locally cached file (for the specified URL) for deletion. If this function succeeds, the local file cache is no longer valid. This function fails if there are any handles opened against the file either by the same process or by a different process on the local computer.

If the item that is named in the <i>URLName</i> parameter is not present in the cache, <b>DavInvalidateCache</b> returns ERROR_SUCCESS without invalidating the cache.