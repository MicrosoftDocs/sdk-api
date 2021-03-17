---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.GetTypeLabel
title: ISyncMgrSyncItemInfo::GetTypeLabel (syncmgr.h)
description: Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string.
helpviewer_keywords: ["GetTypeLabel","GetTypeLabel method [Windows Shell]","GetTypeLabel method [Windows Shell]","ISyncMgrSyncItemInfo interface","ISyncMgrSyncItemInfo interface [Windows Shell]","GetTypeLabel method","ISyncMgrSyncItemInfo.GetTypeLabel","ISyncMgrSyncItemInfo::GetTypeLabel","_shell_ISyncMgrSyncItemInfo_GetTypeLabel","shell.ISyncMgrSyncItemInfo_GetTypeLabel","syncmgr/ISyncMgrSyncItemInfo::GetTypeLabel"]
old-location: shell\ISyncMgrSyncItemInfo_GetTypeLabel.htm
tech.root: shell
ms.assetid: f93e929f-c25b-4511-9478-57686f9e205b
ms.date: 12/05/2018
ms.keywords: GetTypeLabel, GetTypeLabel method [Windows Shell], GetTypeLabel method [Windows Shell],ISyncMgrSyncItemInfo interface, ISyncMgrSyncItemInfo interface [Windows Shell],GetTypeLabel method, ISyncMgrSyncItemInfo.GetTypeLabel, ISyncMgrSyncItemInfo::GetTypeLabel, _shell_ISyncMgrSyncItemInfo_GetTypeLabel, shell.ISyncMgrSyncItemInfo_GetTypeLabel, syncmgr/ISyncMgrSyncItemInfo::GetTypeLabel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSyncItemInfo::GetTypeLabel
 - syncmgr/ISyncMgrSyncItemInfo::GetTypeLabel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncItemInfo.GetTypeLabel
---

# ISyncMgrSyncItemInfo::GetTypeLabel


## -description

Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string.

## -parameters

### -param ppszTypeLabel [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the label string.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>ppszTypeLabel</i> contains an empty string.

## -remarks

The label value is displayed as the System.Sync.ItemTypeLabel (PKEY_Sync_ItemTypeLabel) property in the folder UI. Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">UpdateItem</a> method is called.

The item is responsible for allocating the string buffer pointed to by <i>ppszTypeLabel</i> through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.