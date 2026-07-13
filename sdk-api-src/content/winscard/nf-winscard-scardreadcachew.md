---
UID: NF:winscard.SCardReadCacheW
title: SCardReadCacheW function (winscard.h)
description: Retrieves the value portion of a name-value pair from the global cache maintained by the Smart Card Resource Manager. (Unicode)
helpviewer_keywords: ["SCardReadCache", "SCardReadCache function [Security]", "SCardReadCacheW", "security.scardreadcache", "winscard/SCardReadCache", "winscard/SCardReadCacheW"]
old-location: security\scardreadcache.htm
tech.root: security
ms.assetid: ffa15036-b6d6-4c0a-8f04-e1900484eb8d
ms.date: 12/05/2018
ms.keywords: SCardReadCache, SCardReadCache function [Security], SCardReadCacheA, SCardReadCacheW, security.scardreadcache, winscard/SCardReadCache, winscard/SCardReadCacheA, winscard/SCardReadCacheW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardReadCacheW (Unicode) and SCardReadCacheA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardReadCacheW
 - winscard/SCardReadCacheW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardReadCache
 - SCardReadCacheA
 - SCardReadCacheW
---

# SCardReadCacheW function


## -description

The <b>SCardReadCache</b> function retrieves the value portion of a name-value pair from the global cache maintained by the <a href="/windows/desktop/SecAuthN/smart-card-resource-manager">Smart Card Resource Manager</a>.

## -parameters

### -param hContext [in]

A handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

### -param CardIdentifier [in]

A pointer to a value that uniquely identifies a smart card. The name-value pair that this function reads from the global cache is associated with this smart card.

### -param FreshnessCounter [in]

The current revision of the cached data.

### -param LookupName [in]

A pointer to a null-terminated string that contains the name portion of the name-value pair for which to retrieve the value portion.

### -param Data [out]

A pointer to an array of byte values that contain the value portion of the name-value pair specified by the <i>LookupName</i> parameter.

### -param DataLen [out]

A pointer to the size, in bytes, of the <i>Data</i> buffer.

## -returns

If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>.

If the function fails, it returns one of the following error codes. For more information, see <a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_CACHE_ITEM_NOT_FOUND</b></dt>
<dt>0x80100070</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was not found in the global cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_CACHE_ITEM_STALE</b></dt>
<dt>0x80100071</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was older than requested and has been deleted from the cache.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardwritecachea">SCardWriteCache</a>

## -remarks

> [!NOTE]
> The winscard.h header defines SCardReadCache as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
