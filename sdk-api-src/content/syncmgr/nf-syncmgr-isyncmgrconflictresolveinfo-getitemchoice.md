---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetItemChoice
title: ISyncMgrConflictResolveInfo::GetItemChoice
author: windows-driver-content
description: Gets the index of an item that the user wants to keep.
old-location: shell\ISyncMgrConflictResolveInfo_GetItemChoice.htm
old-project: shell
ms.assetid: 3c857e53-756b-44c2-b3fa-6d57c21939e7
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetItemChoice, GetItemChoice method [Windows Shell], GetItemChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetItemChoice method, ISyncMgrConflictResolveInfo.GetItemChoice, ISyncMgrConflictResolveInfo::GetItemChoice, _shell_ISyncMgrConflictResolveInfo_GetItemChoice, shell.ISyncMgrConflictResolveInfo_GetItemChoice, syncmgr/ISyncMgrConflictResolveInfo::GetItemChoice
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
-	ISyncMgrConflictResolveInfo.GetItemChoice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictResolveInfo::GetItemChoice


## -description


Gets the index of an item that the user wants to keep.


## -parameters




### -param iChoice [in]

Type: <b>UINT</b>

The item that the user wants to keep.


### -param piChoiceIndex






#### - piChoiceindex [out]

Type: <b>UINT*</b>

The index into the conflict's item array. This value is passed to the resolver for subsequent conflicts in the same conflict set if the user chooses to apply the same operation to all selected conflicts of the same type from the same handler.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/e4485f49-9bcb-47a8-8559-da2217ee1eab">ISyncMgrConflictResolveInfo::SetItemChoices</a>
 

 

