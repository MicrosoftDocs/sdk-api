---
UID: NF:bits3_0.IBitsPeerCacheRecord.IsFileValidated
title: IBitsPeerCacheRecord::IsFileValidated (bits3_0.h)
description: Determines whether the file has been validated.
helpviewer_keywords: ["IBitsPeerCacheRecord interface [BITS]","IsFileValidated method","IBitsPeerCacheRecord.IsFileValidated","IBitsPeerCacheRecord::IsFileValidated","IsFileValidated","IsFileValidated method [BITS]","IsFileValidated method [BITS]","IBitsPeerCacheRecord interface","bits.ibitspeercacherecord_isfilevalidated","bits3_0/IBitsPeerCacheRecord::IsFileValidated"]
old-location: bits\ibitspeercacherecord_isfilevalidated.htm
tech.root: Bits
ms.assetid: f492f009-bef7-412e-8626-ae84cd5ce03f
ms.date: 12/05/2018
ms.keywords: IBitsPeerCacheRecord interface [BITS],IsFileValidated method, IBitsPeerCacheRecord.IsFileValidated, IBitsPeerCacheRecord::IsFileValidated, IsFileValidated, IsFileValidated method [BITS], IsFileValidated method [BITS],IBitsPeerCacheRecord interface, bits.ibitspeercacherecord_isfilevalidated, bits3_0/IBitsPeerCacheRecord::IsFileValidated
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
 - IBitsPeerCacheRecord::IsFileValidated
 - bits3_0/IBitsPeerCacheRecord::IsFileValidated
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
 - IBitsPeerCacheRecord.IsFileValidated
---

# IBitsPeerCacheRecord::IsFileValidated


## -description

Determines whether the file has been validated.



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
File has been validated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
File has not been validated.

</td>
</tr>
</table>

## -remarks

The file is available to serve after you validate the file. To validate the file, call the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate">IBackgroundCopyFile3::SetValidationState</a> method. The file is implicitly validated if the application calls <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> without calling <b>SetValidationState</b>. To remove the file from the cache after validation, see <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-deleteurl">IBitsPeerCacheAdministration::DeleteUrl</a> and <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-deleterecord">IBitsPeerCacheAdministration::DeleteRecord</a>.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacherecord">IBitsPeerCacheRecord</a>
