---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncMgrControl::StartHandlerSync


## -description


Initiates the synchronization of all items managed by a particular handler.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler to synchronize. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the window that the handler can use to display any necessary UI. This value can be <b>NULL</b>.


### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> to be passed to <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">Synchronize</a>. This parameter can be <b>NULL</b>.


### -param nSyncControlFlags [in]

Type: <b><a href="https://msdn.microsoft.com/2191c105-788d-434e-a3c1-4f7b7dc543c4">SYNCMGR_SYNC_CONTROL_FLAGS</a></b>

A member of the <a href="https://msdn.microsoft.com/2191c105-788d-434e-a3c1-4f7b7dc543c4">SYNCMGR_SYNC_CONTROL_FLAGS</a> enumeration that specifies whether an item found in both a current sync and a queued sync should be synchronized again when the queued sync is performed.


### -param pResult [in]

Type: <b><a href="https://msdn.microsoft.com/ec48eeda-5af2-4b9b-bf36-f42a6fe46fb0">ISyncMgrSyncResult</a>*</b>

A pointer to an instance of <a href="https://msdn.microsoft.com/ec48eeda-5af2-4b9b-bf36-f42a6fe46fb0">ISyncMgrSyncResult</a>, whose <a href="https://msdn.microsoft.com/8ba7de05-0703-4bab-bf64-ae84f42fad69">Result</a> method is called when the synchronization ends, either through success, failure, or cancellation. The <b>Result</b> method is called with the aggregated state of the handler synchronization. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



