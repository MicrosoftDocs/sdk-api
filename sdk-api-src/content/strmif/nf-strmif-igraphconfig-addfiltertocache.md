---
UID: NF:strmif.IGraphConfig.AddFilterToCache
title: IGraphConfig::AddFilterToCache (strmif.h)
description: The AddFilterToCache method adds a filter to the filter cache.
helpviewer_keywords: ["AddFilterToCache","AddFilterToCache method [DirectShow]","AddFilterToCache method [DirectShow]","IGraphConfig interface","IGraphConfig interface [DirectShow]","AddFilterToCache method","IGraphConfig.AddFilterToCache","IGraphConfig::AddFilterToCache","IGraphConfigAddFilterToCache","dshow.igraphconfig_addfiltertocache","strmif/IGraphConfig::AddFilterToCache"]
old-location: dshow\igraphconfig_addfiltertocache.htm
tech.root: dshow
ms.assetid: 8d5c6d55-1628-462b-828a-50541b6da3e7
ms.date: 12/05/2018
ms.keywords: AddFilterToCache, AddFilterToCache method [DirectShow], AddFilterToCache method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],AddFilterToCache method, IGraphConfig.AddFilterToCache, IGraphConfig::AddFilterToCache, IGraphConfigAddFilterToCache, dshow.igraphconfig_addfiltertocache, strmif/IGraphConfig::AddFilterToCache
f1_keywords:
- strmif/IGraphConfig.AddFilterToCache
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IGraphConfig.AddFilterToCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphConfig::AddFilterToCache


## -description



The <code>AddFilterToCache</code> method adds a filter to the filter cache.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Filter is already in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Filter was added to the cache.

</td>
</tr>
</table>
 




## -remarks



You must disconnect all of the filter's pins before calling this method, or the method will fail. If the filter is in the filter graph, this method will remove it. This method will also put the filter into a stopped state, if it is not already.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>
 

 

