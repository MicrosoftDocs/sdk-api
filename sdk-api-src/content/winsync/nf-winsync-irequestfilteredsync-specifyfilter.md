---
UID: NF:winsync.IRequestFilteredSync.SpecifyFilter
title: IRequestFilteredSync::SpecifyFilter (winsync.h)
author: windows-sdk-content
description: When implemented by a derived class, negotiates which filter is used by the source provider during change enumeration.
old-location: winsync\irequestfilteredsync_specifyfilter.htm
tech.root: winsync
ms.assetid: 653e953f-3f08-4d65-85d5-3c5466361ea5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRequestFilteredSync interface [Windows Sync],SpecifyFilter method, IRequestFilteredSync.SpecifyFilter, IRequestFilteredSync::SpecifyFilter, SpecifyFilter, SpecifyFilter method [Windows Sync], SpecifyFilter method [Windows Sync],IRequestFilteredSync interface, winsync.irequestfilteredsync_specifyfilter, winsync/IRequestFilteredSync::SpecifyFilter
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IRequestFilteredSync.SpecifyFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<li>During processing of <b>IRequestFilteredSync::SpecifyFilter</b>, the destination provider passes filters to <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IFilterRequestCallback::RequestFilter</a>.</li>
<li>During processing of <b>IFilterRequestCallback::RequestFilter</b>, a synchronization session typically calls <a href="https://msdn.microsoft.com/00a533fa-2a91-46e8-9754-af162a5e59ec">ISupportFilteredSync::AddFilter</a> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.

<div class="alert"><b>Note</b>  An implementation of this method can repeatedly call <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IFilterRequestCallback::RequestFilter</a> until a filter is found that is supported by both the destination provider and the source provider. The source provider indicates that it does not support a filter by returning <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_FILTER_NOT_SUPPORTED</a> in response to the <a href="https://msdn.microsoft.com/00a533fa-2a91-46e8-9754-af162a5e59ec">ISupportFilteredSync::AddFilter</a> call.

<p class="note">When <a href="https://msdn.microsoft.com/00a533fa-2a91-46e8-9754-af162a5e59ec">ISupportFilteredSync::AddFilter</a> returns an error other than <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_FILTER_NOT_SUPPORTED</a>, <b>IRequestFilteredSync::SpecifyFilter</b> should return the error to the Sync Application. This ends the synchronization session.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/11ba822e-63d6-4947-8e21-7134bdbcbdc0">IFilterRequestCallback Interface</a>



<a href="https://msdn.microsoft.com/e4b76bb3-d572-4441-94db-7088e881ede2">IRequestFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/cf07e322-7c75-49a4-a514-b4c782ceb2d7">ISupportFilteredSync Interface</a>
 

 

