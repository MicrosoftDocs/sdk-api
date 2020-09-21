---
UID: NF:strmif.IGraphConfig.EnumCacheFilter
title: IGraphConfig::EnumCacheFilter (strmif.h)
description: The EnumCacheFilter method enumerates the filters in the filter cache.
helpviewer_keywords: ["EnumCacheFilter","EnumCacheFilter method [DirectShow]","EnumCacheFilter method [DirectShow]","IGraphConfig interface","IGraphConfig interface [DirectShow]","EnumCacheFilter method","IGraphConfig.EnumCacheFilter","IGraphConfig::EnumCacheFilter","IGraphConfigEnumCacheFilter","dshow.igraphconfig_enumcachefilter","strmif/IGraphConfig::EnumCacheFilter"]
old-location: dshow\igraphconfig_enumcachefilter.htm
tech.root: dshow
ms.assetid: 1782def0-13ed-411c-ab05-d0f0c307e16a
ms.date: 12/05/2018
ms.keywords: EnumCacheFilter, EnumCacheFilter method [DirectShow], EnumCacheFilter method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],EnumCacheFilter method, IGraphConfig.EnumCacheFilter, IGraphConfig::EnumCacheFilter, IGraphConfigEnumCacheFilter, dshow.igraphconfig_enumcachefilter, strmif/IGraphConfig::EnumCacheFilter
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphConfig::EnumCacheFilter
 - strmif/IGraphConfig::EnumCacheFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphConfig.EnumCacheFilter
---

# IGraphConfig::EnumCacheFilter


## -description

The <code>EnumCacheFilter</code> method enumerates the filters in the filter cache.

## -parameters

### -param pEnum [out]

Receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ienumfilters">IEnumFilters</a> interface on the filter enumerator. The caller must release the interface.

## -returns

Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>