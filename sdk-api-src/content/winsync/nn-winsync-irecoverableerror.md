---
UID: NN:winsync.IRecoverableError
title: IRecoverableError
author: windows-driver-content
description: Represents a recoverable error that occurred when an item was loaded or when an item was saved.
old-location: winsync\irecoverableerror.htm
old-project: winsync
ms.assetid: a8b8a84a-6083-4696-bef1-46145a4d71c8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IRecoverableError, IRecoverableError interface [Windows Sync], IRecoverableError interface [Windows Sync], described, winsync.irecoverableerror, winsync/IRecoverableError
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IRecoverableError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IRecoverableError interface


## -description


Represents a recoverable error that occurred when an item was loaded or when an item was saved.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRecoverableError</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRecoverableError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRecoverableError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7ddc479-1428-43d9-9a26-4166cf4eec3d">GetChangeWithRecoverableError</a>
</td>
<td align="left" width="63%">
Gets the item change that caused the error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48ecfc21-ab30-45c7-879b-c2487288419f">GetProvider</a>
</td>
<td align="left" width="63%">
Gets the role of the provider that skipped the item change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6fbc99f-ae01-4f5e-b22c-bd802520ae39">GetRecoverableErrorDataForChange</a>
</td>
<td align="left" width="63%">
Gets additional data about the recoverable error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/609ecdb0-b135-474f-b959-9ab6f427e5d6">GetRecoverableErrorDataForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets additional data about the recoverable error for a specified change unit.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ddfb151-37f1-4df2-827a-11bc6f23ace6">GetStage</a>
</td>
<td align="left" width="63%">
Gets the stage in the synchronization session when the error occurred.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

