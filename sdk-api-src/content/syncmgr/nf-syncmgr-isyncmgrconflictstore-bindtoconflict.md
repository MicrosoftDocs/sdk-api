---
UID: NF:syncmgr.ISyncMgrConflictStore.BindToConflict
title: ISyncMgrConflictStore::BindToConflict method
author: windows-driver-content
description: Binds to a particular conflict specified by IID.
old-location: shell\ISyncMgrConflictStore_BindToConflict.htm
old-project: shell
ms.assetid: 86414360-7dc5-4819-8372-0cede07ba41b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: BindToConflict method [Windows Shell], BindToConflict method [Windows Shell], ISyncMgrConflictStore interface, BindToConflict,ISyncMgrConflictStore.BindToConflict, ISyncMgrConflictStore, ISyncMgrConflictStore interface [Windows Shell], BindToConflict method, ISyncMgrConflictStore::BindToConflict, _shell_ISyncMgrConflictStore_BindToConflict, shell.ISyncMgrConflictStore_BindToConflict, syncmgr/ISyncMgrConflictStore::BindToConflict
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
-	ISyncMgrConflictStore.BindToConflict
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictStore::BindToConflict method


## -description


Binds to a particular conflict specified by IID.


## -parameters




### -param pConflictIdInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a>*</b>


          A pointer to a <a href="https://msdn.microsoft.com/9a54ef7e-0b22-436e-891b-80610ddaef00">SYNCMGR_CONFLICT_ID_INFO</a> structure.
        


### -param riid [in]

Type: <b>REFIID</b>


          A reference to a desired conflict IID.
        


### -param ppv [out]

Type: <b>void**</b>


          When this method returns, contains the interface pointer requested in <i>riid</i>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used when the conflict folder binds to a conflict, given its pointer to an item identifier list (PIDL) or parsing name. The ID is obtained from a conflict that was previously extracted from the store. See <a href="https://msdn.microsoft.com/a5806a83-b470-4617-961d-b768160afc48">ISyncMgrConflict</a>.



