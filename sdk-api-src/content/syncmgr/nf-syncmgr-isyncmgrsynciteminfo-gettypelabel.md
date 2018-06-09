---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.GetTypeLabel
title: ISyncMgrSyncItemInfo::GetTypeLabel
author: windows-sdk-content
description: Gets a label for the item type. This typically provides the model of the device or an equivalent item-specific identity string.
old-location: shell\ISyncMgrSyncItemInfo_GetTypeLabel.htm
old-project: shell
ms.assetid: f93e929f-c25b-4511-9478-57686f9e205b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetTypeLabel, GetTypeLabel method [Windows Shell], GetTypeLabel method [Windows Shell],ISyncMgrSyncItemInfo interface, ISyncMgrSyncItemInfo interface [Windows Shell],GetTypeLabel method, ISyncMgrSyncItemInfo.GetTypeLabel, ISyncMgrSyncItemInfo::GetTypeLabel, _shell_ISyncMgrSyncItemInfo_GetTypeLabel, shell.ISyncMgrSyncItemInfo_GetTypeLabel, syncmgr/ISyncMgrSyncItemInfo::GetTypeLabel
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
 - ISyncMgrSyncItemInfo.GetTypeLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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



The label value is displayed as the System.Sync.ItemTypeLabel (PKEY_Sync_ItemTypeLabel) property in the folder UI. Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> or <a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">UpdateItem</a> method is called.

The item is responsible for allocating the string buffer pointed to by <i>ppszTypeLabel</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.



