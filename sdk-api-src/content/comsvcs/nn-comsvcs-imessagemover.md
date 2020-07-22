---
UID: NN:comsvcs.IMessageMover
title: IMessageMover (comsvcs.h)
description: Moves messages from one queue to another queue.
helpviewer_keywords: ["IMessageMover","IMessageMover interface [COM+]","IMessageMover interface [COM+]","described","_cos_IMessageMover","comsvcs/IMessageMover","cos.imessagemover"]
old-location: cos\imessagemover.htm
tech.root: cos
ms.assetid: aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7
ms.date: 12/05/2018
ms.keywords: IMessageMover, IMessageMover interface [COM+], IMessageMover interface [COM+],described, _cos_IMessageMover, comsvcs/IMessageMover, cos.imessagemover
f1_keywords:
- comsvcs/IMessageMover
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- ComSvcs.h
api_name:
- IMessageMover
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMessageMover interface


## -description


Moves messages from one queue to another queue.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageMover</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMessageMover</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageMover</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-get_commitbatchsize">get_CommitBatchSize</a>
</td>
<td align="left" width="63%">
Retrieves the commit batch size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-get_destpath">get_DestPath</a>
</td>
<td align="left" width="63%">
Retrieves the path of the destination (output) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-get_sourcepath">get_SourcePath</a>
</td>
<td align="left" width="63%">
Retrieves the current path of the source (input) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-movemessages">MoveMessages</a>
</td>
<td align="left" width="63%">
Moves all messages from the source queue to the destination queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-put_commitbatchsize">put_CommitBatchSize</a>
</td>
<td align="left" width="63%">
Sets the commit batch size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-put_destpath">put_DestPath</a>
</td>
<td align="left" width="63%">
Sets the path of the destination (output) queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-put_sourcepath">put_SourcePath</a>
</td>
<td align="left" width="63%">
Sets the path of the source (input) queue.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iplaybackcontrol">IPlaybackControl</a>
 

 

