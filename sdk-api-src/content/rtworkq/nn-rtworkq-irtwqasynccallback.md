---
UID: NN:rtworkq.IRtwqAsyncCallback
title: IRtwqAsyncCallback (rtworkq.h)
description: Callback interface to notify the application when an asynchronous method completes.
helpviewer_keywords: ["IRtwqAsyncCallback","IRtwqAsyncCallback interface","IRtwqAsyncCallback interface","described","base.irtwqasynccallback","rtworkq/IRtwqAsyncCallback"]
old-location: base\irtwqasynccallback.htm
tech.root: backup
ms.assetid: E595C072-98F8-4231-9C8F-A8393D751DE6
ms.date: 12/05/2018
ms.keywords: IRtwqAsyncCallback, IRtwqAsyncCallback interface, IRtwqAsyncCallback interface,described, base.irtwqasynccallback, rtworkq/IRtwqAsyncCallback
f1_keywords:
- rtworkq/IRtwqAsyncCallback
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
- IRtwqAsyncCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRtwqAsyncCallback interface


## -description


Callback interface to notify the application when an asynchronous method completes.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRtwqAsyncCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRtwqAsyncCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasynccallback-getparameters">GetParameters</a>
</td>
<td align="left" width="63%">
Provides configuration information to the dispatching thread for a callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Called when an asynchronous operation is completed.

</td>
</tr>
</table> 

