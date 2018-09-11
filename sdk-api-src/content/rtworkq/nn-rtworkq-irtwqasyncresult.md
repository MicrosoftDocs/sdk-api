---
UID: NN:rtworkq.IRtwqAsyncResult
title: IRtwqAsyncResult
author: windows-sdk-content
description: Provides information about the result of an asynchronous operation.
old-location: base\irtwqasyncresult.htm
tech.root: procthread
ms.assetid: AB23282D-D731-48EE-AF55-CC5A513EBA33
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: IRtwqAsyncResult, IRtwqAsyncResult interface, IRtwqAsyncResult interface,described, base.irtwqasyncresult, rtworkq/IRtwqAsyncResult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRtwqAsyncResult interface


## -description


Provides information about the result of an asynchronous operation.
         


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRtwqAsyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRtwqAsyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRtwqAsyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EF872EDD-4263-4835-81E4-0A61F18E9202">GetObject</a>
</td>
<td align="left" width="63%">
Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26940ECA-BE6A-42E4-8D9E-E002A6D5DD23">GetState</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DF41E4E7-015C-469A-A94F-16F06445B804">GetStateNoAddRef</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method, without incrementing the object's reference count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90E965E5-29E6-4FC9-A923-FBBCC12195E2">GetStatus</a>
</td>
<td align="left" width="63%">
Returns the status of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F3A74F5-615B-40B2-8E69-145D0ECA22A9">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the asynchronous operation.

</td>
</tr>
</table> 

