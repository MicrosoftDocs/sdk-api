---
UID: NF:winsync.IFilterRequestCallback.RequestFilter
title: IFilterRequestCallback::RequestFilter (winsync.h)
description: Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration.
helpviewer_keywords: ["IFilterRequestCallback interface [Windows Sync]","RequestFilter method","IFilterRequestCallback.RequestFilter","IFilterRequestCallback::RequestFilter","RequestFilter","RequestFilter method [Windows Sync]","RequestFilter method [Windows Sync]","IFilterRequestCallback interface","winsync.ifilterrequestcallback_requestfilter","winsync/IFilterRequestCallback::RequestFilter"]
old-location: winsync\ifilterrequestcallback_requestfilter.htm
tech.root: winsync
ms.assetid: f7dea17e-ab13-4eb3-8354-3dfefea16062
ms.date: 12/05/2018
ms.keywords: IFilterRequestCallback interface [Windows Sync],RequestFilter method, IFilterRequestCallback.RequestFilter, IFilterRequestCallback::RequestFilter, RequestFilter, RequestFilter method [Windows Sync], RequestFilter method [Windows Sync],IFilterRequestCallback interface, winsync.ifilterrequestcallback_requestfilter, winsync/IFilterRequestCallback::RequestFilter
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterRequestCallback::RequestFilter
 - winsync/IFilterRequestCallback::RequestFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IFilterRequestCallback.RequestFilter
---

# IFilterRequestCallback::RequestFilter


## -description

Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration.

## -parameters

### -param pFilter [in]

The filter that is specified by the destination provider. This filter is passed to the source provider to be used during change enumeration.

### -param filteringType [in]

A <a href="/windows/win32/api/winsync/ne-winsync-filtering_type">FILTERING_TYPE</a> enumeration value that indicates the type of information that is included in a change batch during filtered synchronization.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_FILTER_NOT_SUPPPORTED</b></dt>
</dl>
</td>
<td width="60%">
When the filter that is specified by <i>pFilter</i> is not supported by the source provider. This is also returned when the source provider does not implement <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportfilteredsync">ISupportFilteredSync</a>.

</td>
</tr>
</table>

## -remarks

Filter negotiation is achieved by using the following steps:

<ol>
<li>Before the source provider begins enumerating changes, starts filter negotiation by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-irequestfilteredsync-specifyfilter">IRequestFilteredSync::SpecifyFilter</a> on the destination provider.</li>
<li>During processing of <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-irequestfilteredsync-specifyfilter">IRequestFilteredSync::SpecifyFilter</a>, the destination provider passes filters to <b>IFilterRequestCallback::RequestFilter</b>.</li>
<li>During processing of <b>IFilterRequestCallback::RequestFilter</b>, calls <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportfilteredsync-addfilter">ISupportFilteredSync::AddFilter</a> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.

## -see-also

<a href="/windows/win32/api/winsync/ne-winsync-filtering_type">FILTERING_TYPE Enumeration</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifilterrequestcallback">IFilterRequestCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irequestfilteredsync">IRequestFilteredSync Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportfilteredsync">ISupportFilteredSync Interface</a>