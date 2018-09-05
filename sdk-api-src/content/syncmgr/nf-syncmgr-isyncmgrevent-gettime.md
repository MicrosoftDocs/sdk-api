---
UID: NF:syncmgr.ISyncMgrEvent.GetTime
title: ISyncMgrEvent::GetTime
author: windows-sdk-content
description: Gets the creation time.
old-location: shell\ISyncMgrEvent_GetTime.htm
old-project: shell
ms.assetid: 1cfe8555-4c63-443a-b3da-e671f8e343d4
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetTime, GetTime method [Windows Shell], GetTime method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetTime method, ISyncMgrEvent.GetTime, ISyncMgrEvent::GetTime, _shell_ISyncMgrEvent_GetTime, shell.ISyncMgrEvent_GetTime, syncmgr/ISyncMgrEvent::GetTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
 - ISyncMgrEvent.GetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetTime


## -description


Gets the creation time.


## -parameters




### -param pfCreationTime [out]

Type: <b>FILETIME*</b>

When this method returns, contains a pointer to a creation time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



