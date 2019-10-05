---
UID: NF:strmif.IGraphConfig.SetFilterFlags
title: IGraphConfig::SetFilterFlags (strmif.h)
author: windows-sdk-content
description: The SetFilterFlags method sets a filter's configuration information.
old-location: dshow\igraphconfig_setfilterflags.htm
tech.root: DirectShow
ms.assetid: 1f2ed50e-8bb9-4076-ad0e-a7311acb8285
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGraphConfig interface [DirectShow],SetFilterFlags method, IGraphConfig.SetFilterFlags, IGraphConfig::SetFilterFlags, IGraphConfigSetFilterFlags, SetFilterFlags, SetFilterFlags method [DirectShow], SetFilterFlags method [DirectShow],IGraphConfig interface, dshow.igraphconfig_setfilterflags, strmif/IGraphConfig::SetFilterFlags
ms.topic: method
f1_keywords: 
 - "strmif/IGraphConfig.SetFilterFlags"
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
 - IGraphConfig.SetFilterFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphConfig::SetFilterFlags


## -description



The <code>SetFilterFlags</code> method sets a filter's configuration information.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of a filter in the filter graph.


### -param dwFlags [in]

Value specifying the new configuration flags. Must be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>No flags set.</td>
</tr>
<tr>
<td>AM_FILTER_FLAGS_REMOVABLE</td>
<td>The filter is removable during a dynamic reconnection. For more information, see Remarks.</td>
</tr>
</table>
 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
 




## -remarks



The AM_FILTER_FLAGS_REMOVABLE flag changes the behavior of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a> method. The <b>Reconnect</b> method performs a dynamic reconnection between two pins. If the caller specifies one pin, but leaves the other pin unspecified, <b>Reconnect</b> searches upstream or downstream from the specified pin to find a suitable match. By default, however, the search fails if it reaches a filter that was added to the graph by means of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltergraph-addfilter">IFilterGraph::AddFilter</a> method. To override this behavior, call <code>SetFilterFlags</code> and set the AM_FILTER_FLAGS_REMOVABLE flag on the filter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>
 

 

