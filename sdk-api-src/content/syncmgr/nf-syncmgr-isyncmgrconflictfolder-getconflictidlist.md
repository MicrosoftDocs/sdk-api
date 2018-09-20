---
UID: NF:syncmgr.ISyncMgrConflictFolder.GetConflictIDList
title: ISyncMgrConflictFolder::GetConflictIDList
author: windows-sdk-content
description: Maps a conflict to its IShellItem.
old-location: shell\ISyncMgrConflictFolder_GetConflictIDList.htm
tech.root: shell
ms.assetid: 2a0794dd-ffa6-4a7b-af1a-1605092ead07
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetConflictIDList, GetConflictIDList method [Windows Shell], GetConflictIDList method [Windows Shell],ISyncMgrConflictFolder interface, ISyncMgrConflictFolder interface [Windows Shell],GetConflictIDList method, ISyncMgrConflictFolder.GetConflictIDList, ISyncMgrConflictFolder::GetConflictIDList, _shell_ISyncMgrConflictFolder_GetConflictIDList, shell.ISyncMgrConflictFolder_GetConflictIDList, syncmgr/ISyncMgrConflictFolder::GetConflictIDList
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
 - ISyncMgrConflictFolder.GetConflictIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflictFolder::GetConflictIDList


## -description


Maps a conflict to its <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -parameters




### -param pConflict [in]

Type: <b><a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a> interface.


### -param ppidlConflict [out]

Type: <b>PIDLIST_RELATIVE*</b>

A pointer to a PIDL, specified relative to the folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



