---
UID: NF:strmif.IGraphConfig.EnumCacheFilter
title: IGraphConfig::EnumCacheFilter
author: windows-sdk-content
description: The EnumCacheFilter method enumerates the filters in the filter cache.
old-location: dshow\igraphconfig_enumcachefilter.htm
old-project: DirectShow
ms.assetid: 1782def0-13ed-411c-ab05-d0f0c307e16a
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: EnumCacheFilter, EnumCacheFilter method [DirectShow], EnumCacheFilter method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],EnumCacheFilter method, IGraphConfig.EnumCacheFilter, IGraphConfig::EnumCacheFilter, IGraphConfigEnumCacheFilter, dshow.igraphconfig_enumcachefilter, strmif/IGraphConfig::EnumCacheFilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphConfig::EnumCacheFilter


## -description



The <code>EnumCacheFilter</code> method enumerates the filters in the filter cache.




## -parameters




### -param pEnum [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e105ccff-86c6-45d5-aead-6d303d038e5a">IEnumFilters</a> interface on the filter enumerator. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

