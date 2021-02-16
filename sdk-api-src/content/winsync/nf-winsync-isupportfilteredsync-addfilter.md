---
UID: NF:winsync.ISupportFilteredSync.AddFilter
title: ISupportFilteredSync::AddFilter (winsync.h)
description: Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class.
helpviewer_keywords: ["AddFilter","AddFilter method [Windows Sync]","AddFilter method [Windows Sync]","ISupportFilteredSync interface","ISupportFilteredSync interface [Windows Sync]","AddFilter method","ISupportFilteredSync.AddFilter","ISupportFilteredSync::AddFilter","winsync.isupportfilteredsync_addfilter","winsync/ISupportFilteredSync::AddFilter"]
old-location: winsync\isupportfilteredsync_addfilter.htm
tech.root: winsync
ms.assetid: 00a533fa-2a91-46e8-9754-af162a5e59ec
ms.date: 12/05/2018
ms.keywords: AddFilter, AddFilter method [Windows Sync], AddFilter method [Windows Sync],ISupportFilteredSync interface, ISupportFilteredSync interface [Windows Sync],AddFilter method, ISupportFilteredSync.AddFilter, ISupportFilteredSync::AddFilter, winsync.isupportfilteredsync_addfilter, winsync/ISupportFilteredSync::AddFilter
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
 - ISupportFilteredSync::AddFilter
 - winsync/ISupportFilteredSync::AddFilter
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
 - ISupportFilteredSync.AddFilter
---

# ISupportFilteredSync::AddFilter


## -description

Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class.

## -parameters

### -param pFilter [in]

The filter that is used for change enumeration by the source provider.

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
<dt><b>SYNC_E_FILTER_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
When the type of filter that is specified by <i>pFilter</i> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

Filter negotiation is achieved by using the following steps:

<ol>
<li>Before the source provider begins enumerating changes, a synchronization session typically starts filter negotiation by calling <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IRequestFilteredSync::SpecifyFilter</a> on the destination provider.</li>
<li>During processing of <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IRequestFilteredSync::SpecifyFilter</a>, the destination provider passes filters to <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IFilterRequestCallback::RequestFilter</a>.</li>
<li>During processing of <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IFilterRequestCallback::RequestFilter</a>, a synchronization session typically calls <b>ISupportFilteredSync::AddFilter</b> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.

<div class="alert"><b>Note</b>  An implementation of this method can examine the filter specified by <i>pFilter</i> and <i>filteringType</i>, and return <a href="/previous-versions/windows/desktop/winsync/windows-sync-error-codes">SYNC_E_FILTER_NOT_SUPPORTED</a> to indicate that the filter is not supported. The destination provider can then request different filters until one is found that is supported.<p class="note">Typically the destination provider will end the synchronization session when an error other than <a href="/previous-versions/windows/desktop/winsync/windows-sync-error-codes">SYNC_E_FILTER_NOT_SUPPORTED</a> is returned from <b>ISupportFilteredSync::AddFilter</b>.

</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/winsync/ne-winsync-filtering_type">FILTERING_TYPE Enumeration</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifilterrequestcallback">IFilterRequestCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irequestfilteredsync">IRequestFilteredSync Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportfilteredsync">ISupportFilteredSync Interface</a>