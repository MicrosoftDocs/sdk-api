---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepItems
title: ISyncMgrResolutionHandler::KeepItems
author: windows-sdk-content
description: Keeps the Shell items that are passed in.
old-location: shell\ISyncMgrResolutionHandler_KeepItems.htm
tech.root: shell
ms.assetid: 81be006b-4aa4-42da-ae1b-001ae92a3e9b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepItems method, ISyncMgrResolutionHandler.KeepItems, ISyncMgrResolutionHandler::KeepItems, KeepItems, KeepItems method [Windows Shell], KeepItems method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepItems, shell.ISyncMgrResolutionHandler_KeepItems, syncmgr/ISyncMgrResolutionHandler::KeepItems
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
 - ISyncMgrResolutionHandler.KeepItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncmgr.h
: 
- ISyncMgrResolutionHandler.KeepItems
: 
---

# ISyncMgrResolutionHandler::KeepItems


## -description


Keeps the Shell items that are passed in.


## -parameters




### -param pArray [in]

Type: <b><a href="https://msdn.microsoft.com/5295ebe5-ec37-4070-80eb-5513b519a0c1">ISyncMgrConflictResolutionItems</a>*</b>

A pointer to an array of<a href="https://msdn.microsoft.com/5295ebe5-ec37-4070-80eb-5513b519a0c1">ISyncMgrConflictResolutionItems</a>. The array will contain more than one item if method <a href="https://msdn.microsoft.com/f178c4d9-0c83-4569-81fe-fe38ac13f0b5">ISyncMgrResolutionHandler::QueryAbilities</a> returned SYNCMGR_RA_KEEP_MULTIPLE in parameter <i>pdwAbilities</i>.


### -param pFeedback [out]

Type: <b><a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/9526cac8-0df3-40b2-9f86-1a4dadb61dcc">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.



