---
UID: NF:syncmgr.ISyncMgrConflictFolder.GetConflictIDList
title: ISyncMgrConflictFolder::GetConflictIDList (syncmgr.h)
author: windows-sdk-content
description: Maps a conflict to its IShellItem.
old-location: shell\ISyncMgrConflictFolder_GetConflictIDList.htm
tech.root: shell
ms.assetid: 2a0794dd-ffa6-4a7b-af1a-1605092ead07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetConflictIDList, GetConflictIDList method [Windows Shell], GetConflictIDList method [Windows Shell],ISyncMgrConflictFolder interface, ISyncMgrConflictFolder interface [Windows Shell],GetConflictIDList method, ISyncMgrConflictFolder.GetConflictIDList, ISyncMgrConflictFolder::GetConflictIDList, _shell_ISyncMgrConflictFolder_GetConflictIDList, shell.ISyncMgrConflictFolder_GetConflictIDList, syncmgr/ISyncMgrConflictFolder::GetConflictIDList
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrConflictFolder.GetConflictIDList"
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
 - ISyncMgrConflictFolder.GetConflictIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrConflictFolder::GetConflictIDList


## -description


Maps a conflict to its <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.


## -parameters




### -param pConflict [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a> interface.


### -param ppidlConflict [out]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to a PIDL, specified relative to the folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



