---
UID: NN:winsync.IFilterRequestCallback
title: IFilterRequestCallback (winsync.h)
author: windows-sdk-content
description: Mediates filter negotiation between a destination provider and a source provider.
old-location: winsync\ifilterrequestcallback.htm
tech.root: winsync
ms.assetid: 11ba822e-63d6-4947-8e21-7134bdbcbdc0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterRequestCallback, IFilterRequestCallback interface [Windows Sync], IFilterRequestCallback interface [Windows Sync],described, winsync.ifilterrequestcallback, winsync/IFilterRequestCallback
ms.topic: interface
f1_keywords: ["winsync/IFilterRequestCallback"]
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
 - IFilterRequestCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterRequestCallback interface


## -description


Mediates filter negotiation between a destination provider and a source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterRequestCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterRequestCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterRequestCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ifilterrequestcallback-requestfilter">RequestFilter</a>
</td>
<td align="left" width="63%">
Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-irequestfilteredsync">IRequestFilteredSync Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportfilteredsync">ISupportFilteredSync Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

