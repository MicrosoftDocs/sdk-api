---
UID: NF:syncmgr.ISyncMgrResolutionHandler.RemoveFromSyncSet
title: ISyncMgrResolutionHandler::RemoveFromSyncSet
author: windows-sdk-content
description: Deletes the conflict and removes the IShellItem from synchronization.
old-location: shell\ISyncMgrResolutionHandler_RemoveFromSyncSet.htm
old-project: shell
ms.assetid: 3f65f844-efa2-43b9-91f2-c9c0ed4e3a9e
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],RemoveFromSyncSet method, ISyncMgrResolutionHandler.RemoveFromSyncSet, ISyncMgrResolutionHandler::RemoveFromSyncSet, RemoveFromSyncSet, RemoveFromSyncSet method [Windows Shell], RemoveFromSyncSet method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_RemoveFromSyncSet, shell.ISyncMgrResolutionHandler_RemoveFromSyncSet, syncmgr/ISyncMgrResolutionHandler::RemoveFromSyncSet
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrResolutionHandler.RemoveFromSyncSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrResolutionHandler::RemoveFromSyncSet


## -description


Deletes the conflict and removes the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>  from synchronization.


## -parameters




### -param pFeedback [out]

Type: <b><a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that is in conflict will no longer be synchronized and the conflict should be deleted.

The <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.



