---
UID: NN:rtworkq.IRtwqAsyncCallback
title: IRtwqAsyncCallback
author: windows-sdk-content
description: Callback interface to notify the application when an asynchronous method completes.
old-location: base\irtwqasynccallback.htm
tech.root: ProcThread
ms.assetid: E595C072-98F8-4231-9C8F-A8393D751DE6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IRtwqAsyncCallback, IRtwqAsyncCallback interface, IRtwqAsyncCallback interface,described, base.irtwqasynccallback, rtworkq/IRtwqAsyncCallback
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
 - IRtwqAsyncCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRtwqAsyncCallback interface


## -description


Callback interface to notify the application when an asynchronous method completes.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRtwqAsyncCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRtwqAsyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRtwqAsyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6569BC4-E722-418E-B469-B20877F44648">GetParameters</a>
</td>
<td align="left" width="63%">
Provides configuration information to the dispatching thread for a callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1798C338-4C82-42A7-AE15-ADFD356604BD">Invoke</a>
</td>
<td align="left" width="63%">
Called when an asynchronous operation is completed.

</td>
</tr>
</table> 

