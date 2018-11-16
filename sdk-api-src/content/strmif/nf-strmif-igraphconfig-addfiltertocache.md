---
UID: NF:strmif.IGraphConfig.AddFilterToCache
title: IGraphConfig::AddFilterToCache
author: windows-sdk-content
description: The AddFilterToCache method adds a filter to the filter cache.
old-location: dshow\igraphconfig_addfiltertocache.htm
tech.root: DirectShow
ms.assetid: 8d5c6d55-1628-462b-828a-50541b6da3e7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddFilterToCache, AddFilterToCache method [DirectShow], AddFilterToCache method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],AddFilterToCache method, IGraphConfig.AddFilterToCache, IGraphConfig::AddFilterToCache, IGraphConfigAddFilterToCache, dshow.igraphconfig_addfiltertocache, strmif/IGraphConfig::AddFilterToCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IGraphConfig.AddFilterToCache
: 
---

# IGraphConfig::AddFilterToCache


## -description



The <code>AddFilterToCache</code> method adds a filter to the filter cache.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

