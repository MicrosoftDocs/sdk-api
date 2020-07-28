---
UID: NN:objidl.IProgressNotify
title: IProgressNotify (objidl.h)
description: Enables applications and other objects to receive notifications of changes in the progress of a downloading operation.
helpviewer_keywords: ["IProgressNotify","IProgressNotify interface [COM]","IProgressNotify interface [COM]","described","_com_iprogressnotify","com.iprogressnotify","objidl/IProgressNotify"]
old-location: com\iprogressnotify.htm
tech.root: com
ms.assetid: 3f90437d-df8f-42b2-af81-519bfb9577b1
ms.date: 12/05/2018
ms.keywords: IProgressNotify, IProgressNotify interface [COM], IProgressNotify interface [COM],described, _com_iprogressnotify, com.iprogressnotify, objidl/IProgressNotify
f1_keywords:
- objidl/IProgressNotify
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
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
- ObjIdl.h
api_name:
- IProgressNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProgressNotify interface


## -description


Enables applications and other objects to receive notifications of changes in the progress of a downloading operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProgressNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProgressNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iprogressnotify-onprogress">OnProgress</a>
</td>
<td align="left" width="63%">
Notifies registered objects and applications of the progress of a downloading operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iprogressnotify-onprogress">IProgressNotify::OnProgress</a>
 

 

