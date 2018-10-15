---
UID: NF:syncmgr.ISyncMgrSyncItemContainer.GetSyncItemCount
title: ISyncMgrSyncItemContainer::GetSyncItemCount
author: windows-sdk-content
description: Gets a count of the sync items in the container.
old-location: shell\ISyncMgrSyncItemContainer_GetSyncItemCount.htm
tech.root: shell
ms.assetid: bbe37dff-d758-41ca-872d-4607d605011d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetSyncItemCount, GetSyncItemCount method [Windows Shell], GetSyncItemCount method [Windows Shell],ISyncMgrSyncItemContainer interface, ISyncMgrSyncItemContainer interface [Windows Shell],GetSyncItemCount method, ISyncMgrSyncItemContainer.GetSyncItemCount, ISyncMgrSyncItemContainer::GetSyncItemCount, _shell_ISyncMgrSyncItemContainer_GetSyncItemCount, shell.ISyncMgrSyncItemContainer_GetSyncItemCount, syncmgr/ISyncMgrSyncItemContainer::GetSyncItemCount
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
 - ISyncMgrSyncItemContainer.GetSyncItemCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncItemContainer::GetSyncItemCount


## -description


Gets a count of the sync items in the container.


## -parameters




### -param pcItems [out]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of items in the container. This is the number of items enumerated by <a href="https://msdn.microsoft.com/0d1695e2-6936-4f53-9594-e0e2bc69afd4">IEnumSyncMgrSyncItems</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



