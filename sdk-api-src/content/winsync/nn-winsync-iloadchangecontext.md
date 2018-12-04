---
UID: NN:winsync.ILoadChangeContext
title: ILoadChangeContext
author: windows-sdk-content
description: Represents information about a change to be loaded from the item store.
old-location: winsync\iloadchangecontext.htm
tech.root: winsync
ms.assetid: 11d8971b-354f-4347-9d3f-6d32df8dc9d2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ILoadChangeContext, ILoadChangeContext interface [Windows Sync], ILoadChangeContext interface [Windows Sync],described, winsync.iloadchangecontext, winsync/ILoadChangeContext
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
 - ILoadChangeContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILoadChangeContext interface


## -description


Represents information about a change to be loaded from the item store.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILoadChangeContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILoadChangeContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILoadChangeContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac425bc-f6ec-4a95-b351-01f9eb27a744">GetSyncChange</a>
</td>
<td align="left" width="63%">
Gets the change item for which the change data should be retrieved from the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e557889-a4f6-4e05-99ce-bb05013dc4cd">SetRecoverableErrorOnChange</a>
</td>
<td align="left" width="63%">
Indicates that a recoverable error occurred when data for this item was loaded from the item store.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0489a26c-5760-4e41-84c9-45868d27b67c">SetRecoverableErrorOnChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

