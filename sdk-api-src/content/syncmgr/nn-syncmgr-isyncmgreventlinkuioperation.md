---
UID: NN:syncmgr.ISyncMgrEventLinkUIOperation
title: ISyncMgrEventLinkUIOperation (syncmgr.h)
description: Provides a method that is called when event links are clicked in the sync results folder.
old-location: shell\ISyncMgrEventLinkUIOperation.htm
tech.root: shell
ms.assetid: 53ea9488-77e0-4eb2-86d3-88747ba44654
ms.date: 12/05/2018
ms.keywords: ISyncMgrEventLinkUIOperation, ISyncMgrEventLinkUIOperation interface [Windows Shell], ISyncMgrEventLinkUIOperation interface [Windows Shell],described, _shell_ISyncMgrEventLinkUIOperation, shell.ISyncMgrEventLinkUIOperation, syncmgr/ISyncMgrEventLinkUIOperation
ms.topic: interface
f1_keywords:
- syncmgr/ISyncMgrEventLinkUIOperation
dev_langs:
- c++
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
- Syncmgr.h
api_name:
- ISyncMgrEventLinkUIOperation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrEventLinkUIOperation interface


## -description


Provides a method that is called when event links are clicked in the sync results folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEventLinkUIOperation</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>. <b>ISyncMgrEventLinkUIOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrEventLinkUIOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgreventlinkuioperation-init">Init</a>
</td>
<td align="left" width="63%">
Enables Sync Center to provide the event to link to so <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgruioperation-run">ISyncMgrUIOperation::Run</a>  knows which event to operate upon.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface, from which it inherits.

Sync Center calls <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_EventLinkClick for the object ID.



