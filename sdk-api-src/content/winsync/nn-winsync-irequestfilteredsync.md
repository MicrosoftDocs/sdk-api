---
UID: NN:winsync.IRequestFilteredSync
title: IRequestFilteredSync
author: windows-sdk-content
description: When implemented by a derived class, represents a destination provider that can specify a filter to be used by the source provider during change enumeration.
old-location: winsync\irequestfilteredsync.htm
tech.root: winsync
ms.assetid: e4b76bb3-d572-4441-94db-7088e881ede2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRequestFilteredSync, IRequestFilteredSync interface [Windows Sync], IRequestFilteredSync interface [Windows Sync],described, winsync.irequestfilteredsync, winsync/IRequestFilteredSync
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRequestFilteredSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRequestFilteredSync interface


## -description


When implemented by a derived class, represents a destination provider that can specify a filter to be used by the source provider during change enumeration.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRequestFilteredSync</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRequestFilteredSync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRequestFilteredSync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/653e953f-3f08-4d65-85d5-3c5466361ea5">SpecifyFilter</a>
</td>
<td align="left" width="63%">
Negotiates which filter is used by the source provider during change enumeration.


</td>
</tr>
</table> 


## -remarks



Typically, <b>IRequestFilteredSync</b> is implemented by a destination provider.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

