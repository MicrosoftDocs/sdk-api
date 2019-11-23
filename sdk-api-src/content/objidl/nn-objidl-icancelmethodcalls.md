---
UID: NN:objidl.ICancelMethodCalls
title: ICancelMethodCalls (objidl.h)

description: Manages cancellation requests on an outbound method call and monitors the current state of that method call on the server thread.
old-location: com\icancelmethodcalls.htm
tech.root: com
ms.assetid: 5e31f706-1c9c-4510-845c-4e47093780a1

ms.date: 12/05/2018
ms.keywords: ICancelMethodCalls, ICancelMethodCalls interface [COM], ICancelMethodCalls interface [COM],described, _com_icancelmethodcalls, com.icancelmethodcalls, objidlbase/ICancelMethodCalls
ms.topic: interface
f1_keywords: 
 - "objidl/ICancelMethodCalls"
dev_langs:
 - c++
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.Idl
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
 - objidlbase.h
api_name:
 - ICancelMethodCalls
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICancelMethodCalls interface


## -description


Manages cancellation requests on an outbound method call and monitors the current state of that method call on the server thread.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICancelMethodCalls</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICancelMethodCalls</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICancelMethodCalls</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icancelmethodcalls-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Requests that a method call be canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-icancelmethodcalls-testcancel">TestCancel</a>
</td>
<td align="left" width="63%">
Determines whether a call has been canceled.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imessagefilter">IMessageFilter</a>
 

 

