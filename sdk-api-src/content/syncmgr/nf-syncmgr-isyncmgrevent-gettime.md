---
UID: NF:syncmgr.ISyncMgrEvent.GetTime
title: ISyncMgrEvent::GetTime (syncmgr.h)
description: Gets the creation time.
helpviewer_keywords: ["GetTime","GetTime method [Windows Shell]","GetTime method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetTime method","ISyncMgrEvent.GetTime","ISyncMgrEvent::GetTime","_shell_ISyncMgrEvent_GetTime","shell.ISyncMgrEvent_GetTime","syncmgr/ISyncMgrEvent::GetTime"]
old-location: shell\ISyncMgrEvent_GetTime.htm
tech.root: shell
ms.assetid: 1cfe8555-4c63-443a-b3da-e671f8e343d4
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [Windows Shell], GetTime method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetTime method, ISyncMgrEvent.GetTime, ISyncMgrEvent::GetTime, _shell_ISyncMgrEvent_GetTime, shell.ISyncMgrEvent_GetTime, syncmgr/ISyncMgrEvent::GetTime
f1_keywords:
- syncmgr/ISyncMgrEvent.GetTime
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
- ISyncMgrEvent.GetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrEvent::GetTime


## -description


Gets the creation time.


## -parameters




### -param pfCreationTime [out]

Type: <b>FILETIME*</b>

When this method returns, contains a pointer to a creation time as a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



