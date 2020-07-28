---
UID: NF:syncmgr.ISyncMgrSyncItemContainer.GetSyncItemCount
title: ISyncMgrSyncItemContainer::GetSyncItemCount (syncmgr.h)
description: Gets a count of the sync items in the container.
helpviewer_keywords: ["GetSyncItemCount","GetSyncItemCount method [Windows Shell]","GetSyncItemCount method [Windows Shell]","ISyncMgrSyncItemContainer interface","ISyncMgrSyncItemContainer interface [Windows Shell]","GetSyncItemCount method","ISyncMgrSyncItemContainer.GetSyncItemCount","ISyncMgrSyncItemContainer::GetSyncItemCount","_shell_ISyncMgrSyncItemContainer_GetSyncItemCount","shell.ISyncMgrSyncItemContainer_GetSyncItemCount","syncmgr/ISyncMgrSyncItemContainer::GetSyncItemCount"]
old-location: shell\ISyncMgrSyncItemContainer_GetSyncItemCount.htm
tech.root: shell
ms.assetid: bbe37dff-d758-41ca-872d-4607d605011d
ms.date: 12/05/2018
ms.keywords: GetSyncItemCount, GetSyncItemCount method [Windows Shell], GetSyncItemCount method [Windows Shell],ISyncMgrSyncItemContainer interface, ISyncMgrSyncItemContainer interface [Windows Shell],GetSyncItemCount method, ISyncMgrSyncItemContainer.GetSyncItemCount, ISyncMgrSyncItemContainer::GetSyncItemCount, _shell_ISyncMgrSyncItemContainer_GetSyncItemCount, shell.ISyncMgrSyncItemContainer_GetSyncItemCount, syncmgr/ISyncMgrSyncItemContainer::GetSyncItemCount
f1_keywords:
- syncmgr/ISyncMgrSyncItemContainer.GetSyncItemCount
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncItemContainer::GetSyncItemCount


## -description


Gets a count of the sync items in the container.


## -parameters




### -param pcItems [out]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of items in the container. This is the number of items enumerated by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



