---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.GetComment
title: ISyncMgrSyncItemInfo::GetComment
author: windows-sdk-content
description: Gets a string that contains commentary regarding the item.
old-location: shell\ISyncMgrSyncItemInfo_GetComment.htm
old-project: shell
ms.assetid: 3959784b-2926-43fd-b8e5-bb1884e5d321
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetComment, GetComment method [Windows Shell], GetComment method [Windows Shell],ISyncMgrSyncItemInfo interface, ISyncMgrSyncItemInfo interface [Windows Shell],GetComment method, ISyncMgrSyncItemInfo.GetComment, ISyncMgrSyncItemInfo::GetComment, _shell_ISyncMgrSyncItemInfo_GetComment, shell.ISyncMgrSyncItemInfo_GetComment, syncmgr/ISyncMgrSyncItemInfo::GetComment
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
 - ISyncMgrSyncItemInfo.GetComment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItemInfo::GetComment


## -description


Gets a string that contains commentary regarding the item.


## -parameters




### -param ppszComment [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the comment string. This string is of maximum length MAX_SYNCMGR_NAME including the terminating null character.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>ppszComment</i> contains an empty string.




## -remarks



This string could be provided by an item to display a summary of its contents, for example, "32 contacts" or "13 songs". The string can have a maximum length of MAX_SYNCMGR_NAME including the terminating null character.

The comment value is displayed as the System.Sync.Comments (PKEY_Sync_Comments) property in the folder UI when a synchronization is not being performed.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.

The item is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.



