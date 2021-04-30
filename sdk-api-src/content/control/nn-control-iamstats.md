---
UID: NN:control.IAMStats
title: IAMStats (control.h)
description: The IAMStats interface retrieves performance data from the Filter Graph Manager.
helpviewer_keywords: ["IAMStats","IAMStats interface [DirectShow]","IAMStats interface [DirectShow]","described","IAMStatsInterface","control/IAMStats","dshow.iamstats"]
old-location: dshow\iamstats.htm
tech.root: dshow
ms.assetid: 01dbaba2-fdca-4f42-8816-fd99c4364dbd
ms.date: 12/05/2018
ms.keywords: IAMStats, IAMStats interface [DirectShow], IAMStats interface [DirectShow],described, IAMStatsInterface, control/IAMStats, dshow.iamstats
req.header: control.h
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
 - IAMStats
 - control/IAMStats
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
 - IAMStats
---

# IAMStats interface


## -description

The <code>IAMStats</code> interface retrieves performance data from the Filter Graph Manager. Filters can use this interface to record performance data.

<b>Filter developers</b>: As with all Filter Graph Manager interfaces, a filter must not hold a reference count on this interface, or it will cause a circular reference count. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-joinfiltergraph">IBaseFilter::JoinFilterGraph</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMStats</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMStats</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

Each statistic is defined by a name and an index. Use the <b>GetIndex</b> method to find the index from the name. Values are always <b>double</b> types. The following statistics are predefined.

<table>
<tr>
<th>Name
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>RenderFile</td>
<td>Measures the time taken by each call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>.</td>
</tr>
<tr>
<td>ConnectDirectInternal</td>
<td>Measures the time taken to connect two filters.</td>
</tr>
<tr>
<td>Build Mapper Cache</td>
<td>Measures the time taken to cache information about registered filters (used by the <a href="/windows/desktop/DirectShow/filter-mapper">Filter Mapper</a> object).</td>
</tr>
<tr>
<td>Process Category <i>CategoryName</i></td>
<td>Measures the time taken to cache information about filters in a particular category, where <i>CategoryName</i> is the friendly name of the filter category. (See <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.)</td>
</tr>
</table>
 

For each of these statistics, the values represent time in milliseconds.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
