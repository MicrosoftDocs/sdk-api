---
UID: NF:syncmgr.ISyncMgrConflictResolutionItems.GetItem
title: ISyncMgrConflictResolutionItems::GetItem
author: windows-sdk-content
description: Gets result information for a specified item, when successful.
old-location: shell\ISyncMgrConflictResolutionItems_GetItem.htm
tech.root: shell
ms.assetid: c98ec4fa-bbca-4213-95c3-b50ccafbbfdb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],ISyncMgrConflictResolutionItems interface, ISyncMgrConflictResolutionItems interface [Windows Shell],GetItem method, ISyncMgrConflictResolutionItems.GetItem, ISyncMgrConflictResolutionItems::GetItem, _shell_ISyncMgrConflictResolutionItems_GetItem, shell.ISyncMgrConflictResolutionItems_GetItem, syncmgr/ISyncMgrConflictResolutionItems::GetItem
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
 - ISyncMgrConflictResolutionItems.GetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflictResolutionItems::GetItem


## -description


Gets result information for a specified item, when successful.


## -parameters




### -param iIndex [in]

Type: <b>UINT</b>

The index of the item.


### -param pItemInfo [out]

Type: <b><a href="https://msdn.microsoft.com/572bb9b7-a33d-4323-9363-abb43d9411e6">CONFIRM_CONFLICT_RESULT_INFO</a>*</b>

On success, contains a pointer to a <a href="https://msdn.microsoft.com/572bb9b7-a33d-4323-9363-abb43d9411e6">CONFIRM_CONFLICT_RESULT_INFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



