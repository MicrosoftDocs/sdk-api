---
UID: NN:winsync.ISupportFilteredSync
title: ISupportFilteredSync (winsync.h)
author: windows-sdk-content
description: When implemented by a derived class, represents a source provider that supports filtered change enumeration, and that can negotiate the type of filter that is used.
old-location: winsync\isupportfilteredsync.htm
tech.root: winsync
ms.assetid: cf07e322-7c75-49a4-a514-b4c782ceb2d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISupportFilteredSync, ISupportFilteredSync interface [Windows Sync], ISupportFilteredSync interface [Windows Sync],described, winsync.isupportfilteredsync, winsync/ISupportFilteredSync
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
 - ISupportFilteredSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISupportFilteredSync interface


## -description


When implemented by a derived class, represents a source provider that supports filtered change enumeration, and that can negotiate the type of filter that is used.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISupportFilteredSync</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISupportFilteredSync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISupportFilteredSync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00a533fa-2a91-46e8-9754-af162a5e59ec">AddFilter</a>
</td>
<td align="left" width="63%">
Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class. 

</td>
</tr>
</table> 


## -remarks



<b>ISupportFilteredSync</b> is typically implemented by a source provider.




## -see-also




<a href="https://msdn.microsoft.com/11ba822e-63d6-4947-8e21-7134bdbcbdc0">IFilterRequestCallback Interface</a>



<a href="https://msdn.microsoft.com/e4b76bb3-d572-4441-94db-7088e881ede2">IRequestFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

