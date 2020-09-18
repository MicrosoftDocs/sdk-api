---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetMaximumCacheSize
title: IBitsPeerCacheAdministration::GetMaximumCacheSize (bits3_0.h)
description: Gets the maximum size of the cache.
helpviewer_keywords: ["GetMaximumCacheSize","GetMaximumCacheSize method [BITS]","GetMaximumCacheSize method [BITS]","IBitsPeerCacheAdministration interface","IBitsPeerCacheAdministration interface [BITS]","GetMaximumCacheSize method","IBitsPeerCacheAdministration.GetMaximumCacheSize","IBitsPeerCacheAdministration::GetMaximumCacheSize","bits.ibitspeercacheadministration_getmaximumcachesize","bits3_0/IBitsPeerCacheAdministration::GetMaximumCacheSize"]
old-location: bits\ibitspeercacheadministration_getmaximumcachesize.htm
tech.root: Bits
ms.assetid: 6ea0e6f7-c674-4088-9085-5f6246681009
ms.date: 12/05/2018
ms.keywords: GetMaximumCacheSize, GetMaximumCacheSize method [BITS], GetMaximumCacheSize method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetMaximumCacheSize method, IBitsPeerCacheAdministration.GetMaximumCacheSize, IBitsPeerCacheAdministration::GetMaximumCacheSize, bits.ibitspeercacheadministration_getmaximumcachesize, bits3_0/IBitsPeerCacheAdministration::GetMaximumCacheSize
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
 - IBitsPeerCacheAdministration::GetMaximumCacheSize
 - bits3_0/IBitsPeerCacheAdministration::GetMaximumCacheSize
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
 - IBitsPeerCacheAdministration.GetMaximumCacheSize
---

# IBitsPeerCacheAdministration::GetMaximumCacheSize


## -description

Gets the maximum size of the cache.

## -parameters

### -param pBytes [out]

Maximum size of the cache, as a percentage of available hard disk drive space.

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



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize">IBitsPeerCacheAdministration::SetMaximumCacheSize</a>