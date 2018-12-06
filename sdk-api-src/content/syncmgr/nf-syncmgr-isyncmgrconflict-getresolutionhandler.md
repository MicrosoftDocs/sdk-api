---
UID: NF:syncmgr.ISyncMgrConflict.GetResolutionHandler
title: ISyncMgrConflict::GetResolutionHandler
author: windows-sdk-content
description: Gets the resolution handler for the conflict.
old-location: shell\ISyncMgrConflict_GetResolutionHandler.htm
tech.root: shell
ms.assetid: 9adbc429-098c-4ba9-af62-54f772be83e3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetResolutionHandler, GetResolutionHandler method [Windows Shell], GetResolutionHandler method [Windows Shell],ISyncMgrConflict interface, ISyncMgrConflict interface [Windows Shell],GetResolutionHandler method, ISyncMgrConflict.GetResolutionHandler, ISyncMgrConflict::GetResolutionHandler, _shell_ISyncMgrConflict_GetResolutionHandler, shell.ISyncMgrConflict_GetResolutionHandler, syncmgr/ISyncMgrConflict::GetResolutionHandler
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
 - ISyncMgrConflict.GetResolutionHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflict::GetResolutionHandler


## -description


Gets the resolution handler for the conflict.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

A reference to the ID for the resolution handler.


### -param ppvResolutionHandler [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



