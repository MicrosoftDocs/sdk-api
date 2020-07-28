---
UID: NF:strmif.IGraphConfig.GetFilterFlags
title: IGraphConfig::GetFilterFlags (strmif.h)
description: The GetFilterFlags method retrieves a filter's configuration information.
helpviewer_keywords: ["GetFilterFlags","GetFilterFlags method [DirectShow]","GetFilterFlags method [DirectShow]","IGraphConfig interface","IGraphConfig interface [DirectShow]","GetFilterFlags method","IGraphConfig.GetFilterFlags","IGraphConfig::GetFilterFlags","IGraphConfigGetFilterFlags","dshow.igraphconfig_getfilterflags","strmif/IGraphConfig::GetFilterFlags"]
old-location: dshow\igraphconfig_getfilterflags.htm
tech.root: dshow
ms.assetid: 747c3865-1969-45e8-a2c9-dbd72a9ea463
ms.date: 12/05/2018
ms.keywords: GetFilterFlags, GetFilterFlags method [DirectShow], GetFilterFlags method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],GetFilterFlags method, IGraphConfig.GetFilterFlags, IGraphConfig::GetFilterFlags, IGraphConfigGetFilterFlags, dshow.igraphconfig_getfilterflags, strmif/IGraphConfig::GetFilterFlags
f1_keywords:
- strmif/IGraphConfig.GetFilterFlags
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
- IGraphConfig.GetFilterFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphConfig::GetFilterFlags


## -description



The <code>GetFilterFlags</code> method retrieves a filter's configuration information.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of a filter in the filter graph.


### -param pdwFlags [out]

Receives the current configuration flags.


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
Null pointer argument.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter is not in the graph.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-setfilterflags">IGraphConfig::SetFilterFlags</a>
 

 

