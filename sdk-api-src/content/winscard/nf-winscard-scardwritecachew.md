---
UID: NF:winscard.SCardWriteCacheW
title: SCardWriteCacheW function (winscard.h)
description: Writes a name-value pair from a smart card to the global cache maintained by the Smart Card Resource Manager. (Unicode)
helpviewer_keywords: ["SCardWriteCache", "SCardWriteCache function [Security]", "SCardWriteCacheW", "security.scardwritecache", "winscard/SCardWriteCache", "winscard/SCardWriteCacheW"]
old-location: security\scardwritecache.htm
tech.root: security
ms.assetid: e982e297-6a78-41f4-a81c-d207a96f1dab
ms.date: 12/05/2018
ms.keywords: SCardWriteCache, SCardWriteCache function [Security], SCardWriteCacheA, SCardWriteCacheW, security.scardwritecache, winscard/SCardWriteCache, winscard/SCardWriteCacheA, winscard/SCardWriteCacheW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardWriteCacheW (Unicode) and SCardWriteCacheA (ANSI)
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
 - SCardWriteCacheW
 - winscard/SCardWriteCacheW
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
 - SCardWriteCache
 - SCardWriteCacheA
 - SCardWriteCacheW
---

# SCardWriteCacheW function


## -description

The <b>SCardWriteCache</b> function writes a name-value pair from a smart card to the global cache maintained by the <a href="/windows/desktop/SecAuthN/smart-card-resource-manager">Smart Card Resource Manager</a>.

## -parameters

### -param hContext [in]

A handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

### -param CardIdentifier [in]

A pointer to a value that uniquely identifies the smart card from which the name-value pair was read.

### -param FreshnessCounter [in]

The current revision of the cached data.

### -param LookupName [in]

A pointer to a null-terminated string that contains the name portion of the name-value pair to write to the global cache.

### -param Data [in]

A pointer to an array of byte values that contain the value portion of the name-value pair to write to the global cache.

### -param DataLen [in]

The size, in bytes, of the <i>Data</i> buffer.

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
<dt><b>SCARD_W_CACHE_ITEM_TOO_BIG</b></dt>
<dt>0x80100072</dt>
</dl>
</td>
<td width="60%">
The size of the specified name-value pair exceeds the maximum size defined for the global cache.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardreadcachea">SCardReadCache</a>

## -remarks

> [!NOTE]
> The winscard.h header defines SCardWriteCache as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
