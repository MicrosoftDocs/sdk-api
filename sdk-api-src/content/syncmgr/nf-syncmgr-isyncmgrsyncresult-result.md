---
UID: NF:syncmgr.ISyncMgrSyncResult.Result
title: ISyncMgrSyncResult::Result (syncmgr.h)
author: windows-sdk-content
description: Gets the result of a StartHandlerSync or StartItemSync call.
old-location: shell\ISyncMgrSyncResult_Result.htm
tech.root: shell
ms.assetid: 8ba7de05-0703-4bab-bf64-ae84f42fad69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncResult interface [Windows Shell],Result method, ISyncMgrSyncResult.Result, ISyncMgrSyncResult::Result, Result, Result method [Windows Shell], Result method [Windows Shell],ISyncMgrSyncResult interface, _shell_ISyncMgrSyncResult_Result, shell.ISyncMgrSyncResult_Result, syncmgr/ISyncMgrSyncResult::Result
ms.topic: method
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
 - ISyncMgrSyncResult.Result
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncResult::Result


## -description


Gets the result of a <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">StartHandlerSync</a> or <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">StartItemSync</a> call.


## -parameters




### -param nStatus [in]

Type: <b><a href="https://msdn.microsoft.com/78622014-643e-4449-b937-a6122a06f470">SYNCMGR_PROGRESS_STATUS</a></b>

The current status of the progress report. See <a href="https://msdn.microsoft.com/78622014-643e-4449-b937-a6122a06f470">SYNCMGR_PROGRESS_STATUS</a>.


### -param cError [in]

Type: <b>UINT</b>

An error.


### -param cConflicts [in]

Type: <b>UINT</b>

Specifies conflicts.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



