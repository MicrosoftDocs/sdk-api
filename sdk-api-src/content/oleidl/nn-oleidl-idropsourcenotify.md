---
UID: NN:oleidl.IDropSourceNotify
title: IDropSourceNotify (oleidl.h)
description: The IDropSourceNotify interface is implemented on an IDropSource object to receive notifications from OLE when a user drags the mouse into or out of a potential drop target window.helpviewer_keywords: ["IDropSourceNotify","IDropSourceNotify interface [COM]","IDropSourceNotify interface [COM]","described","_ole_idropsourcenotify","com.idropsourcenotify","oleidl/IDropSourceNotify"]
old-location: com\idropsourcenotify.htm
tech.root: com
ms.assetid: 62ef4fe6-3871-41ef-9542-6fe9f3bed21c
ms.date: 12/05/2018
ms.keywords: IDropSourceNotify, IDropSourceNotify interface [COM], IDropSourceNotify interface [COM],described, _ole_idropsourcenotify, com.idropsourcenotify, oleidl/IDropSourceNotify
f1_keywords:
- oleidl/IDropSourceNotify
dev_langs:
- c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
- OleIdl.h
api_name:
- IDropSourceNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDropSourceNotify interface


## -description


The <b>IDropSourceNotify</b> interface is implemented on an <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a> object to receive notifications from OLE when a user drags the mouse into or out of a potential drop target window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropSourceNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDropSourceNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDropSourceNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idropsourcenotify-dragentertarget">DragEnterTarget</a>
</td>
<td align="left" width="63%">
OLE calls this method when the user drags the mouse cursor into a potential drop target window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-idropsourcenotify-dragleavetarget">DragLeaveTarget</a>
</td>
<td align="left" width="63%">
OLE calls this method when the user drags the mouse cursor out of a potential drop target window.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a>
 

 

