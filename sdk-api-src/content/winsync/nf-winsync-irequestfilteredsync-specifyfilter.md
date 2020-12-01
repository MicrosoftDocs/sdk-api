---
UID: NF:winsync.IRequestFilteredSync.SpecifyFilter
title: IRequestFilteredSync::SpecifyFilter (winsync.h)
description: When implemented by a derived class, negotiates which filter is used by the source provider during change enumeration.
helpviewer_keywords: ["IRequestFilteredSync interface [Windows Sync]","SpecifyFilter method","IRequestFilteredSync.SpecifyFilter","IRequestFilteredSync::SpecifyFilter","SpecifyFilter","SpecifyFilter method [Windows Sync]","SpecifyFilter method [Windows Sync]","IRequestFilteredSync interface","winsync.irequestfilteredsync_specifyfilter","winsync/IRequestFilteredSync::SpecifyFilter"]
old-location: winsync\irequestfilteredsync_specifyfilter.htm
tech.root: winsync
ms.assetid: 653e953f-3f08-4d65-85d5-3c5466361ea5
ms.date: 12/05/2018
ms.keywords: IRequestFilteredSync interface [Windows Sync],SpecifyFilter method, IRequestFilteredSync.SpecifyFilter, IRequestFilteredSync::SpecifyFilter, SpecifyFilter, SpecifyFilter method [Windows Sync], SpecifyFilter method [Windows Sync],IRequestFilteredSync interface, winsync.irequestfilteredsync_specifyfilter, winsync/IRequestFilteredSync::SpecifyFilter
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
 - IRequestFilteredSync::SpecifyFilter
 - winsync/IRequestFilteredSync::SpecifyFilter
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
 - IRequestFilteredSync.SpecifyFilter
---

# IRequestFilteredSync::SpecifyFilter


## -description

When implemented by a derived class, negotiates which filter is used by the source provider during change enumeration.

## -parameters

### -param pCallback [in]

The callback interface that is used by the destination provider to request that a filter be used by the source provider during change enumeration.

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
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

Filter negotiation is achieved by using the following steps:

<ol>
<li>Before the source provider begins enumerating changes, a synchronization session typically starts filter negotiation by calling <b>IRequestFilteredSync::SpecifyFilter</b> on the destination provider.</li>
<li>During processing of <b>IRequestFilteredSync::SpecifyFilter</b>, the destination provider passes filters to <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IFilterRequestCallback::RequestFilter</a>.</li>
<li>During processing of <b>IFilterRequestCallback::RequestFilter</b>, a synchronization session typically calls <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportfilteredsync-addfilter">ISupportFilteredSync::AddFilter</a> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.

<div class="alert"><b>Note</b>  An implementation of this method can repeatedly call <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">IFilterRequestCallback::RequestFilter</a> until a filter is found that is supported by both the destination provider and the source provider. The source provider indicates that it does not support a filter by returning <a href="/previous-versions/windows/desktop/winsync/windows-sync-error-codes">SYNC_E_FILTER_NOT_SUPPORTED</a> in response to the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportfilteredsync-addfilter">ISupportFilteredSync::AddFilter</a> call.

<p class="note">When <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportfilteredsync-addfilter">ISupportFilteredSync::AddFilter</a> returns an error other than <a href="/previous-versions/windows/desktop/winsync/windows-sync-error-codes">SYNC_E_FILTER_NOT_SUPPORTED</a>, <b>IRequestFilteredSync::SpecifyFilter</b> should return the error to the Sync Application. This ends the synchronization session.

</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifilterrequestcallback">IFilterRequestCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irequestfilteredsync">IRequestFilteredSync Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportfilteredsync">ISupportFilteredSync Interface</a>