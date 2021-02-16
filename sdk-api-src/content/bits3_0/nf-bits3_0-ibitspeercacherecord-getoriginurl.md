---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetOriginUrl
title: IBitsPeerCacheRecord::GetOriginUrl (bits3_0.h)
description: Gets the origin URL of the cached file.
helpviewer_keywords: ["GetOriginUrl","GetOriginUrl method [BITS]","GetOriginUrl method [BITS]","IBitsPeerCacheRecord interface","IBitsPeerCacheRecord interface [BITS]","GetOriginUrl method","IBitsPeerCacheRecord.GetOriginUrl","IBitsPeerCacheRecord::GetOriginUrl","bits.ibitspeercacherecord_getoriginurl","bits3_0/IBitsPeerCacheRecord::GetOriginUrl"]
old-location: bits\ibitspeercacherecord_getoriginurl.htm
tech.root: Bits
ms.assetid: 9d74df3a-89e0-4a3a-82f3-c2e79c609b21
ms.date: 12/05/2018
ms.keywords: GetOriginUrl, GetOriginUrl method [BITS], GetOriginUrl method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetOriginUrl method, IBitsPeerCacheRecord.GetOriginUrl, IBitsPeerCacheRecord::GetOriginUrl, bits.ibitspeercacherecord_getoriginurl, bits3_0/IBitsPeerCacheRecord::GetOriginUrl
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitsPeerCacheRecord::GetOriginUrl
 - bits3_0/IBitsPeerCacheRecord::GetOriginUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheRecord.GetOriginUrl
---

# IBitsPeerCacheRecord::GetOriginUrl


## -description

Gets the origin URL of the cached file.

## -parameters

### -param pVal [in]

Null-terminated string that contains the origin URL of the cached file. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppOriginUrl</i> when done.

## -returns

The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

This URL may be different than the URL originally specified in the BITS job if <a href="/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">IBackgroundCopyJobHttpOptions::SetSecurityFlags</a> is set to BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT or BG_HTTP_REDIRECT_POLICY_DISALLOW.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a>