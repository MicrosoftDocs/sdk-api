---
UID: NN:ctxtcall.IContextCallback
title: IContextCallback (ctxtcall.h)
description: Provides a mechanism to execute a function inside a specific COM+ object context.
helpviewer_keywords: ["IContextCallback","IContextCallback interface [COM]","IContextCallback interface [COM]","described","_com_icontextcallback","com.icontextcallback","ctxtcall/IContextCallback"]
old-location: com\icontextcallback.htm
tech.root: com
ms.assetid: 47af7b80-3419-4a40-8932-a5a27f297dc9
ms.date: 12/05/2018
ms.keywords: IContextCallback, IContextCallback interface [COM], IContextCallback interface [COM],described, _com_icontextcallback, com.icontextcallback, ctxtcall/IContextCallback
req.header: ctxtcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextCallback
 - ctxtcall/IContextCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctxtcall.h
api_name:
 - IContextCallback
---

# IContextCallback interface


## -description

Provides a mechanism to execute a function inside a specific COM+ object context.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctxtcall/nf-ctxtcall-icontextcallback-contextcallback">ContextCallback</a>
</td>
<td align="left" width="63%">
Enters the object context, executes the specified function, and returns.

</td>
</tr>
</table>

## -remarks

 An instance of this interface for the current context can be obtained using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.

