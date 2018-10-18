---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepRecent
title: ISyncMgrResolutionHandler::KeepRecent
author: windows-sdk-content
description: Keeps the more recent copy.
old-location: shell\ISyncMgrResolutionHandler_KeepRecent.htm
tech.root: shell
ms.assetid: a2327234-4a8d-42b4-aa62-f5c286e3c24b
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepRecent method, ISyncMgrResolutionHandler.KeepRecent, ISyncMgrResolutionHandler::KeepRecent, KeepRecent, KeepRecent method [Windows Shell], KeepRecent method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepRecent, shell.ISyncMgrResolutionHandler_KeepRecent, syncmgr/ISyncMgrResolutionHandler::KeepRecent
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
 - ISyncMgrResolutionHandler.KeepRecent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrResolutionHandler::KeepRecent


## -description


Keeps the more recent copy.


## -parameters




### -param pFeedback [out]

Type: <b><a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



