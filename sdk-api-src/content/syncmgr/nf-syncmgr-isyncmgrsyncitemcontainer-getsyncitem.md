---
UID: NF:syncmgr.ISyncMgrSyncItemContainer.GetSyncItem
title: ISyncMgrSyncItemContainer::GetSyncItem
author: windows-driver-content
description: Gets a specified sync item.
old-location: shell\ISyncMgrSyncItemContainer_GetSyncItem.htm
old-project: shell
ms.assetid: 27cdfcfe-d419-4232-b1cc-b9e7b8b2d315
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetSyncItem, GetSyncItem method [Windows Shell], GetSyncItem method [Windows Shell],ISyncMgrSyncItemContainer interface, ISyncMgrSyncItemContainer interface [Windows Shell],GetSyncItem method, ISyncMgrSyncItemContainer.GetSyncItem, ISyncMgrSyncItemContainer::GetSyncItem, _shell_ISyncMgrSyncItemContainer_GetSyncItem, shell.ISyncMgrSyncItemContainer_GetSyncItem, syncmgr/ISyncMgrSyncItemContainer::GetSyncItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrSyncItemContainer.GetSyncItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItemContainer::GetSyncItem


## -description


Gets a specified sync item.


## -parameters




### -param pszItemID




### -param ppItem [out]

Type: <b><a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a> instance representing the sync item.


#### - ppszItemID [in]

Type: <b>LPCWSTR*</b>

A pointer to a buffer containing the item ID representing the desired item. The ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if the handler does not recognize the ID specified at <i>ppszItemID</i>.



