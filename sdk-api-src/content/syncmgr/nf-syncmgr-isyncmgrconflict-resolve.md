---
UID: NF:syncmgr.ISyncMgrConflict.Resolve
title: ISyncMgrConflict::Resolve method
author: windows-driver-content
description: Resolves the conflict using its own sync handler, controls UI.
old-location: shell\ISyncMgrConflict_Resolve.htm
old-project: shell
ms.assetid: 9680b96e-9a83-45e1-a2bf-674aff6490ec
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISyncMgrConflict, ISyncMgrConflict interface [Windows Shell], Resolve method, ISyncMgrConflict::Resolve, Resolve method [Windows Shell], Resolve method [Windows Shell], ISyncMgrConflict interface, Resolve,ISyncMgrConflict.Resolve, _shell_ISyncMgrConflict_Resolve, shell.ISyncMgrConflict_Resolve, syncmgr/ISyncMgrConflict::Resolve
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
-	ISyncMgrConflict.Resolve
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflict::Resolve method


## -description


Resolves the conflict using its own sync handler, controls UI.


## -parameters




### -param pResolveInfo [in]

Type: <b><a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Note that the store must tell the sync center if the conflict was removed by calling <a href="https://msdn.microsoft.com/606df5fb-0c4b-49c7-82ed-28f22927953a">UpdateConflicts</a> after the conflict is resolved. The conflict is assumed to still exist until the store notifies the sync center of changes. The resolution choices for user selection are available through <a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>.



