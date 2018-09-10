---
UID: NF:syncmgr.IEnumSyncMgrConflict.Skip
title: IEnumSyncMgrConflict::Skip
author: windows-sdk-content
description: Skips forward the specified number of conflicts in the enumeration.
old-location: shell\IEnumSyncMgrConflict_Skip.htm
tech.root: shell
ms.assetid: d636dd60-835f-40a8-b2e6-7d7ebf87e897
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IEnumSyncMgrConflict interface [Windows Shell],Skip method, IEnumSyncMgrConflict.Skip, IEnumSyncMgrConflict::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumSyncMgrConflict interface, _shell_IEnumSyncMgrConflict_Skip, shell.IEnumSyncMgrConflict_Skip, syncmgr/IEnumSyncMgrConflict::Skip
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
 - IEnumSyncMgrConflict.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSyncMgrConflict::Skip


## -description


Skips forward the specified number of conflicts in the enumeration.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of conflicts to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



