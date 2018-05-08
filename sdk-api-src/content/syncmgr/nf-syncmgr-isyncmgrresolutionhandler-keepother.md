---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepOther
title: ISyncMgrResolutionHandler::KeepOther
author: windows-driver-content
description: Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.
old-location: shell\ISyncMgrResolutionHandler_KeepOther.htm
old-project: shell
ms.assetid: 6d3e3b01-447c-4f7b-8a63-5bd9084de00a
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepOther method, ISyncMgrResolutionHandler.KeepOther, ISyncMgrResolutionHandler::KeepOther, KeepOther, KeepOther method [Windows Shell], KeepOther method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepOther, shell.ISyncMgrResolutionHandler_KeepOther, syncmgr/ISyncMgrResolutionHandler::KeepOther
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrResolutionHandler.KeepOther
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrResolutionHandler::KeepOther


## -description


Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.


## -parameters




### -param psiOther [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to the substitute <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


### -param pFeedback [out]

Type: <b><a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The specified Shell item that replaces the Shell item(s) in conflict may not have been one of those originally in conflict.  It may be a merged copy, or a replacement copy.

The <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.



