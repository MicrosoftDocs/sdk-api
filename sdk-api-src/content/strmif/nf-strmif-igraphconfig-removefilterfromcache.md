---
UID: NF:strmif.IGraphConfig.RemoveFilterFromCache
title: IGraphConfig::RemoveFilterFromCache
author: windows-sdk-content
description: The RemoveFilterFromCache method removes a filter from the filter cache.
old-location: dshow\igraphconfig_removefilterfromcache.htm
tech.root: DirectShow
ms.assetid: a23710d0-85aa-4ae0-84ea-03b9e22091ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IGraphConfig interface [DirectShow],RemoveFilterFromCache method, IGraphConfig.RemoveFilterFromCache, IGraphConfig::RemoveFilterFromCache, IGraphConfigRemoveFilterFromCache, RemoveFilterFromCache, RemoveFilterFromCache method [DirectShow], RemoveFilterFromCache method [DirectShow],IGraphConfig interface, dshow.igraphconfig_removefilterfromcache, strmif/IGraphConfig::RemoveFilterFromCache
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
 - IGraphConfig.RemoveFilterFromCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfig::RemoveFilterFromCache


## -description



The <code>RemoveFilterFromCache</code> method removes a filter from the filter cache.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of the filter to remove from the cache.


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
Filter was not in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Filter was successfully removed from the cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

