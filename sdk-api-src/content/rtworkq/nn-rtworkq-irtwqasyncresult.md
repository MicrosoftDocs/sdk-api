---
UID: NN:rtworkq.IRtwqAsyncResult
title: IRtwqAsyncResult (rtworkq.h)
description: Provides information about the result of an asynchronous operation.helpviewer_keywords: ["IRtwqAsyncResult","IRtwqAsyncResult interface","IRtwqAsyncResult interface","described","base.irtwqasyncresult","rtworkq/IRtwqAsyncResult"]
old-location: base\irtwqasyncresult.htm
tech.root: ProcThread
ms.assetid: AB23282D-D731-48EE-AF55-CC5A513EBA33
ms.date: 12/05/2018
ms.keywords: IRtwqAsyncResult, IRtwqAsyncResult interface, IRtwqAsyncResult interface,described, base.irtwqasyncresult, rtworkq/IRtwqAsyncResult
f1_keywords:
- rtworkq/IRtwqAsyncResult
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRtwqAsyncResult interface


## -description


Provides information about the result of an asynchronous operation.
         


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRtwqAsyncResult</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRtwqAsyncResult</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-getstate">GetState</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-getstatenoaddref">GetStateNoAddRef</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method, without incrementing the object's reference count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Returns the status of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the asynchronous operation.

</td>
</tr>
</table> 

