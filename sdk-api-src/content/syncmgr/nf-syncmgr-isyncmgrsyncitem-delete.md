---
UID: NF:syncmgr.ISyncMgrSyncItem.Delete
title: ISyncMgrSyncItem::Delete
author: windows-sdk-content
description: Deletes a sync item.
old-location: shell\ISyncMgrSyncItem_Delete.htm
old-project: shell
ms.assetid: 403c01fe-928d-4b9b-a087-6cc68d1aa90a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Delete, Delete method [Windows Shell], Delete method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],Delete method, ISyncMgrSyncItem.Delete, ISyncMgrSyncItem::Delete, _shell_ISyncMgrSyncItem_Delete, shell.ISyncMgrSyncItem_Delete, syncmgr/ISyncMgrSyncItem::Delete
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
 - ISyncMgrSyncItem.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItem::Delete


## -description


Deletes a sync item.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Sync Center calls this method when the user selects the item in the handler's folder and launches its <b>Delete</b> task, but only if the item has set the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_ICM_CAN_DELETE</a> flag. If the handler supports the <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">SYNCMGR_OBJECTID_QueryBeforeDeactivate</a> object, this method is only called if the UI operation was successful.

If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL.



