---
UID: NN:comsvcs.IServicePoolConfig
title: IServicePoolConfig
author: windows-sdk-content
description: Used to configure an object pool.
old-location: cos\iservicepoolconfig.htm
old-project: cossdk
ms.assetid: 026abfcf-56b5-4821-a9d4-37beeb3a052b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServicePoolConfig, IServicePoolConfig interface [COM+], IServicePoolConfig interface [COM+],described, _cos_IServicePoolConfig, comsvcs/IServicePoolConfig, cos.iservicepoolconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePoolConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServicePoolConfig interface


## -description


Used to configure an object pool.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePoolConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServicePoolConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServicePoolConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cef9ff6b-53e2-43e1-9be6-7c0d7f89c318">get_ClassFactory</a>
</td>
<td align="left" width="63%">
Retrieves a class factory for the pooled objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcedf01c-2780-40dc-9ac9-70e267592fa0">get_CreationTimeout</a>
</td>
<td align="left" width="63%">
Retrieves the time-out interval for activating a pooled object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9fb76d4-d153-4968-ad1c-79036b4bb8a4">get_MaxPoolSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/267e2785-dbff-4b44-8bd5-e7e1e8f69478">get_MinPoolSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/329c67f0-3c02-4cea-bee6-b5c8aaa9471b">get_TransactionAffinity</a>
</td>
<td align="left" width="63%">
Determines whether objects involved in transactions are held until the transaction completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/329c67f0-3c02-4cea-bee6-b5c8aaa9471b">put_ClassFactory</a>
</td>
<td align="left" width="63%">
Sets a class factory for the pooled objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04beabf7-831d-4c53-880e-f1fc22f2f20d">put_CreationTimeout</a>
</td>
<td align="left" width="63%">
Sets the time-out interval for activating a pooled object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/618d4969-c29e-4944-8954-a982a90f3c15">put_MaxPoolSize</a>
</td>
<td align="left" width="63%">
Sets the maximum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6280b4ed-704e-464e-bde2-64c1f2353730">put_MinPoolSize</a>
</td>
<td align="left" width="63%">
Sets the minimum number of objects in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f69bae2-560d-455b-b1b4-922c2fb4563a">put_TransactionAffinity</a>
</td>
<td align="left" width="63%">
Sets whether objects involved in transactions are held until the transaction completes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb86ffa5-b4cd-48bc-a99e-245e75ddb9c2">IServicePool</a>
 

 

