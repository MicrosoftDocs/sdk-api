---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepItems
title: ISyncMgrResolutionHandler::KeepItems (syncmgr.h)
author: windows-sdk-content
description: Keeps the Shell items that are passed in.
old-location: shell\ISyncMgrResolutionHandler_KeepItems.htm
tech.root: shell
ms.assetid: 81be006b-4aa4-42da-ae1b-001ae92a3e9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepItems method, ISyncMgrResolutionHandler.KeepItems, ISyncMgrResolutionHandler::KeepItems, KeepItems, KeepItems method [Windows Shell], KeepItems method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepItems, shell.ISyncMgrResolutionHandler_KeepItems, syncmgr/ISyncMgrResolutionHandler::KeepItems
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrResolutionHandler.KeepItems"
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
 - ISyncMgrResolutionHandler.KeepItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrResolutionHandler::KeepItems


## -description


Keeps the Shell items that are passed in.


## -parameters




### -param pArray [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems">ISyncMgrConflictResolutionItems</a>*</b>

A pointer to an array of<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems">ISyncMgrConflictResolutionItems</a>. The array will contain more than one item if method <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities">ISyncMgrResolutionHandler::QueryAbilities</a> returned SYNCMGR_RA_KEEP_MULTIPLE in parameter <i>pdwAbilities</i>.


### -param pFeedback [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.



