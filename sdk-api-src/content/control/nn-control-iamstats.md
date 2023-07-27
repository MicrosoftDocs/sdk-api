---
UID: NN:control.IAMStats
title: IAMStats (control.h)
description: The IAMStats interface retrieves performance data from the Filter Graph Manager.
helpviewer_keywords: ["IAMStats","IAMStats interface [DirectShow]","IAMStats interface [DirectShow]","described","IAMStatsInterface","control/IAMStats","dshow.iamstats"]
old-location: dshow\iamstats.htm
tech.root: dshow
ms.assetid: 01dbaba2-fdca-4f42-8816-fd99c4364dbd
ms.date: 4/26/2023
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

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMStats</code> interface retrieves performance data from the Filter Graph Manager. Filters can use this interface to record performance data.

<b>Filter developers</b>: As with all Filter Graph Manager interfaces, a filter must not hold a reference count on this interface, or it will cause a circular reference count. For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-joinfiltergraph">IBaseFilter::JoinFilterGraph</a>.

## -inheritance

The <b>IAMStats</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAMStats</b> also has these types of members:

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
