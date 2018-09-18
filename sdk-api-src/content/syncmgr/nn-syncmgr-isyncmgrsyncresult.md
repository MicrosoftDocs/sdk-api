---
UID: NN:syncmgr.ISyncMgrSyncResult
title: ISyncMgrSyncResult
author: windows-sdk-content
description: Exposes a method that applications calling ISyncMgrControl can use to get the result of a ISyncMgrControl::StartHandlerSync or ISyncMgrControl::StartItemSync call.
old-location: shell\ISyncMgrSyncResult.htm
tech.root: shell
ms.assetid: ec48eeda-5af2-4b9b-bf36-f42a6fe46fb0
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ISyncMgrSyncResult, ISyncMgrSyncResult interface [Windows Shell], ISyncMgrSyncResult interface [Windows Shell],described, _shell_ISyncMgrSyncResult, shell.ISyncMgrSyncResult, syncmgr/ISyncMgrSyncResult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncResult interface


## -description


Exposes a method that applications calling <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> can use to get the result of a <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">ISyncMgrControl::StartHandlerSync</a> or <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">ISyncMgrControl::StartItemSync</a> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSyncResult</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8ba7de05-0703-4bab-bf64-ae84f42fad69">Result</a>
</td>
<td align="left" width="63%">
Gets the result of a <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">ISyncMgrControl::StartHandlerSync</a> or <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">ISyncMgrControl::StartItemSync</a> call.

</td>
</tr>
</table> 

