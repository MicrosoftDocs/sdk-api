---
UID: NF:winsync.ISupportFilteredSync.AddFilter
title: ISupportFilteredSync::AddFilter (winsync.h)
author: windows-sdk-content
description: Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class.
old-location: winsync\isupportfilteredsync_addfilter.htm
tech.root: winsync
ms.assetid: 00a533fa-2a91-46e8-9754-af162a5e59ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddFilter, AddFilter method [Windows Sync], AddFilter method [Windows Sync],ISupportFilteredSync interface, ISupportFilteredSync interface [Windows Sync],AddFilter method, ISupportFilteredSync.AddFilter, ISupportFilteredSync::AddFilter, winsync.isupportfilteredsync_addfilter, winsync/ISupportFilteredSync::AddFilter
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
 - ISupportFilteredSync.AddFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISupportFilteredSync::AddFilter


## -description


Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class.


## -parameters




### -param pFilter [in]

The filter that is used for change enumeration by the source provider.


### -param filteringType [in]

A <a href="https://msdn.microsoft.com/en-us/library/Dd744771(v=VS.85).aspx">FILTERING_TYPE</a> enumeration value that indicates the type of information that is included in a change batch during filtered synchronization.


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
<li>Before the source provider begins enumerating changes, a synchronization session typically starts filter negotiation by calling <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IRequestFilteredSync::SpecifyFilter</a> on the destination provider.</li>
<li>During processing of <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IRequestFilteredSync::SpecifyFilter</a>, the destination provider passes filters to <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IFilterRequestCallback::RequestFilter</a>.</li>
<li>During processing of <a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">IFilterRequestCallback::RequestFilter</a>, a synchronization session typically calls <b>ISupportFilteredSync::AddFilter</b> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.

<div class="alert"><b>Note</b>  An implementation of this method can examine the filter specified by <i>pFilter</i> and <i>filteringType</i>, and return <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_FILTER_NOT_SUPPORTED</a> to indicate that the filter is not supported. The destination provider can then request different filters until one is found that is supported.<p class="note">Typically the destination provider will end the synchronization session when an error other than <a href="https://msdn.microsoft.com/da86cf89-885b-42bc-9fcb-0c9114a36f78">SYNC_E_FILTER_NOT_SUPPORTED</a> is returned from <b>ISupportFilteredSync::AddFilter</b>.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd744771(v=VS.85).aspx">FILTERING_TYPE Enumeration</a>



<a href="https://msdn.microsoft.com/11ba822e-63d6-4947-8e21-7134bdbcbdc0">IFilterRequestCallback Interface</a>



<a href="https://msdn.microsoft.com/e4b76bb3-d572-4441-94db-7088e881ede2">IRequestFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/cf07e322-7c75-49a4-a514-b4c782ceb2d7">ISupportFilteredSync Interface</a>
 

 

