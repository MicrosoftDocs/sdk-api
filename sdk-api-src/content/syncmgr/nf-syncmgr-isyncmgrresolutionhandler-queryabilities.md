---
UID: NF:syncmgr.ISyncMgrResolutionHandler.QueryAbilities
title: ISyncMgrResolutionHandler::QueryAbilities
author: windows-driver-content
description: Determines what options the conflict presenter will display.
old-location: shell\ISyncMgrResolutionHandler_QueryAbilities.htm
old-project: shell
ms.assetid: f178c4d9-0c83-4569-81fe-fe38ac13f0b5
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],QueryAbilities method, ISyncMgrResolutionHandler.QueryAbilities, ISyncMgrResolutionHandler::QueryAbilities, QueryAbilities, QueryAbilities method [Windows Shell], QueryAbilities method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_QueryAbilities, shell.ISyncMgrResolutionHandler_QueryAbilities, syncmgr/ISyncMgrResolutionHandler::QueryAbilities
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
-	ISyncMgrResolutionHandler.QueryAbilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrResolutionHandler::QueryAbilities


## -description


Determines what options the conflict presenter will display.


## -parameters




### -param pdwAbilities [out]

Type: <b>SYNCMGR_RESOLUTION_ABILITIES_FLAGS*</b>

When this method returns, contains one of the <a href="https://msdn.microsoft.com/5a7ff366-e155-43c0-aafe-f61ad0caf550">SYNCMGR_RESOLUTION_ABILITIES</a> enumerated type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The handler exposes how a conflict can be resolved by calling this method. The result of this method determines what options the conflict presenter displays, and as a result, how other methods in this interface are called.



