---
UID: NN:syncmgr.ISyncMgrSyncResult
title: ISyncMgrSyncResult (syncmgr.h)
description: Exposes a method that applications calling ISyncMgrControl can use to get the result of a ISyncMgrControl::StartHandlerSync or ISyncMgrControl::StartItemSync call.
old-location: shell\ISyncMgrSyncResult.htm
tech.root: shell
ms.assetid: ec48eeda-5af2-4b9b-bf36-f42a6fe46fb0
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncResult, ISyncMgrSyncResult interface [Windows Shell], ISyncMgrSyncResult interface [Windows Shell],described, _shell_ISyncMgrSyncResult, shell.ISyncMgrSyncResult, syncmgr/ISyncMgrSyncResult
ms.topic: interface
f1_keywords:
- syncmgr/ISyncMgrSyncResult
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
- ISyncMgrSyncResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncResult interface


## -description


Exposes a method that applications calling <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> can use to get the result of a <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">ISyncMgrControl::StartHandlerSync</a> or <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">ISyncMgrControl::StartItemSync</a> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncResult</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncresult-result">Result</a>
</td>
<td align="left" width="63%">
Gets the result of a <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">ISyncMgrControl::StartHandlerSync</a> or <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">ISyncMgrControl::StartItemSync</a> call.

</td>
</tr>
</table> 

