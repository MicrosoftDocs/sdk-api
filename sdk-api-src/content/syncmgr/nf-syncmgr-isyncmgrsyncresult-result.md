---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncMgrSyncResult::Result


## -description


Gets the result of a <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">StartHandlerSync</a> or <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">StartItemSync</a> call.


## -parameters




### -param nStatus [in]

Type: <b><a href="https://msdn.microsoft.com/78622014-643e-4449-b937-a6122a06f470">SYNCMGR_PROGRESS_STATUS</a></b>

The current status of the progress report. See <a href="https://msdn.microsoft.com/78622014-643e-4449-b937-a6122a06f470">SYNCMGR_PROGRESS_STATUS</a>.


### -param cError [in]

Type: <b>UINT</b>

An error.


### -param cConflicts [in]

Type: <b>UINT</b>

Specifies conflicts.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



