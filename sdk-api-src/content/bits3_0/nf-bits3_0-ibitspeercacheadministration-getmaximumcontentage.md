---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetMaximumContentAge
title: IBitsPeerCacheAdministration::GetMaximumContentAge (bits3_0.h)
description: Gets the age by when files are removed from the cache.
helpviewer_keywords: ["GetMaximumContentAge","GetMaximumContentAge method [BITS]","GetMaximumContentAge method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","GetMaximumContentAge method","IBitsPeerCacheAdministration.GetMaximumContentAge","IBitsPeerCacheAdministration::GetMaximumContentAge","bits.ibitspeercacheadministration_getmaximumcontentage","bits3_0/IBitsPeerCacheAdministration::GetMaximumContentAge"]
old-location: bits\ibitspeercacheadministration_getmaximumcontentage.htm
tech.root: Bits
ms.assetid: 6b6b0c97-9906-464d-b267-5adde1919a45
ms.date: 12/05/2018
ms.keywords: GetMaximumContentAge, GetMaximumContentAge method [BITS], GetMaximumContentAge method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetMaximumContentAge method, IBitsPeerCacheAdministration.GetMaximumContentAge, IBitsPeerCacheAdministration::GetMaximumContentAge, bits.ibitspeercacheadministration_getmaximumcontentage, bits3_0/IBitsPeerCacheAdministration::GetMaximumContentAge
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
 - IBitsPeerCacheAdministration::GetMaximumContentAge
 - bits3_0/IBitsPeerCacheAdministration::GetMaximumContentAge
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
 - IBitsPeerCacheAdministration.GetMaximumContentAge
---

# IBitsPeerCacheAdministration::GetMaximumContentAge


## -description

Gets the age by when files are removed from the cache.

## -parameters

### -param pSeconds [out]

Age, in seconds. If the last time that the file was accessed is older than this age, BITS removes the file from the cache.

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

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibitspeercacheadministration">IBitsPeerCacheAdministration</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage">IBitsPeerCacheAdministration::SetMaximumContentAge</a>