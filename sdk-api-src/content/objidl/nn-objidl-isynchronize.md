---
UID: NN:objidl.ISynchronize
title: ISynchronize (objidl.h)
description: Provides asynchronous communication between objects about the occurrence of an event.
old-location: com\isynchronize.htm
tech.root: com
ms.assetid: 2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6
ms.date: 12/05/2018
ms.keywords: ISynchronize, ISynchronize interface [COM], ISynchronize interface [COM],described, _com_isynchronize, com.isynchronize, objidlbase/ISynchronize
f1_keywords:
- objidl/ISynchronize
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
req.idl: ObjIdl.idl
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
- ISynchronize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronize interface


## -description


Provides asynchronous communication between objects about the occurrence of an event. Objects that implement <b>ISynchronize</b> can receive indications that an event has occurred, and they can respond to queries about the event. In this way, clients can make sure that one request has been processed before they submit a subsequent request that depends on completion of the first one.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISynchronize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-reset">Reset</a>
</td>
<td align="left" width="63%">
Sets the synchronization object to the nonsignaled state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-signal">Signal</a>
</td>
<td align="left" width="63%">
Sets the synchronization object to the signaled state and causes pending wait operations to return S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-wait">Wait</a>
</td>
<td align="left" width="63%">
Waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isynchronizecontainer">ISynchronizeContainer</a>
 

 

