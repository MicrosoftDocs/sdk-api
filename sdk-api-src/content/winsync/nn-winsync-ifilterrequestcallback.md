---
UID: NN:winsync.IFilterRequestCallback
title: IFilterRequestCallback
author: windows-sdk-content
description: Mediates filter negotiation between a destination provider and a source provider.
old-location: winsync\ifilterrequestcallback.htm
old-project: winsync
ms.assetid: 11ba822e-63d6-4947-8e21-7134bdbcbdc0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IFilterRequestCallback, IFilterRequestCallback interface [Windows Sync], IFilterRequestCallback interface [Windows Sync],described, winsync.ifilterrequestcallback, winsync/IFilterRequestCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IFilterRequestCallback interface


## -description


Mediates filter negotiation between a destination provider and a source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterRequestCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilterRequestCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f7dea17e-ab13-4eb3-8354-3dfefea16062">RequestFilter</a>
</td>
<td align="left" width="63%">
Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e4b76bb3-d572-4441-94db-7088e881ede2">IRequestFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/cf07e322-7c75-49a4-a514-b4c782ceb2d7">ISupportFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

