---
UID: NF:syncmgr.IEnumSyncMgrConflict.Clone
title: IEnumSyncMgrConflict::Clone
author: windows-sdk-content
description: Not used. Clones an IEnumSyncMgrConflict object.
old-location: shell\IEnumSyncMgrConflict_Clone.htm
tech.root: shell
ms.assetid: 2eb0f1c1-71e2-45e6-bef7-1b480efb4ab7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumSyncMgrConflict interface, IEnumSyncMgrConflict interface [Windows Shell],Clone method, IEnumSyncMgrConflict.Clone, IEnumSyncMgrConflict::Clone, _shell_IEnumSyncMgrConflict_Clone, shell.IEnumSyncMgrConflict_Clone, syncmgr/IEnumSyncMgrConflict::Clone
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
 - IEnumSyncMgrConflict.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSyncMgrConflict::Clone


## -description


Not used. Clones an <a href="https://msdn.microsoft.com/627f39be-5c9d-49a1-af73-210cdbb7940a">IEnumSyncMgrConflict</a> object.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/627f39be-5c9d-49a1-af73-210cdbb7940a">IEnumSyncMgrConflict</a>**</b>

The address of the cloned <a href="https://msdn.microsoft.com/627f39be-5c9d-49a1-af73-210cdbb7940a">IEnumSyncMgrConflict</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



