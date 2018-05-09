---
UID: NF:syncmgr.ISyncMgrEvent.GetFlags
title: ISyncMgrEvent::GetFlags
author: windows-driver-content
description: Gets event flags.
old-location: shell\ISyncMgrEvent_GetFlags.htm
old-project: shell
ms.assetid: 51651a03-da3d-4b75-97bf-3be1db56054e
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetFlags, GetFlags method [Windows Shell], GetFlags method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetFlags method, ISyncMgrEvent.GetFlags, ISyncMgrEvent::GetFlags, _shell_ISyncMgrEvent_GetFlags, shell.ISyncMgrEvent_GetFlags, syncmgr/ISyncMgrEvent::GetFlags
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
-	ISyncMgrEvent.GetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetFlags


## -description


Gets event flags.


## -parameters




### -param pnFlags [out]

Type: <b><a href="https://msdn.microsoft.com/bb901a85-8f54-4030-81d5-40af66e490bf">SYNCMGR_EVENT_FLAGS</a>*</b>

When this method returns, contains a pointer to a value that indicates the currently set flags, taken from members of the <a href="https://msdn.microsoft.com/bb901a85-8f54-4030-81d5-40af66e490bf">SYNCMGR_EVENT_FLAGS</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



