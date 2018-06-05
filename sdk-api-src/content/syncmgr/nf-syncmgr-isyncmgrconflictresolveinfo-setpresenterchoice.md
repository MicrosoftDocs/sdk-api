---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.SetPresenterChoice
title: ISyncMgrConflictResolveInfo::SetPresenterChoice
author: windows-sdk-content
description: Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.
old-location: shell\ISyncMgrConflictResolveInfo_SetPresenterChoice.htm
old-project: shell
ms.assetid: 5f4bfe69-1ff3-4d21-9c27-f5d8ecfc8371
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISyncMgrConflictResolveInfo interface [Windows Shell],SetPresenterChoice method, ISyncMgrConflictResolveInfo.SetPresenterChoice, ISyncMgrConflictResolveInfo::SetPresenterChoice, SetPresenterChoice, SetPresenterChoice method [Windows Shell], SetPresenterChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, _shell_ISyncMgrConflictResolveInfo_SetPresenterChoice, shell.ISyncMgrConflictResolveInfo_SetPresenterChoice, syncmgr/ISyncMgrConflictResolveInfo::SetPresenterChoice
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrConflictResolveInfo.SetPresenterChoice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictResolveInfo::SetPresenterChoice


## -description


Sets what kind of choice was made about a sync manager conflict resolution and whether to apply the choice to all subsequent conflicts in the set.


## -parameters




### -param nPresenterChoice [in]

Type: <b><a href="https://msdn.microsoft.com/5e98754b-51d7-4798-9c69-8a9a839c4cda">SYNCMGR_PRESENTER_CHOICE</a></b>

The choice that was made about the conflict resolution. One of the members of the <a href="https://msdn.microsoft.com/5e98754b-51d7-4798-9c69-8a9a839c4cda">SYNCMGR_PRESENTER_CHOICE</a> enumeration.


### -param fApplyToAll [in]

Type: <b>BOOL</b>

If <b>TRUE</b>, then apply the given choice to all subsequent conflicts in the set. In this case, <a href="https://msdn.microsoft.com/e4485f49-9bcb-47a8-8559-da2217ee1eab">ISyncMgrConflictResolveInfo::SetItemChoices</a> must also be called.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/277eee0e-3f75-4ed1-8df2-75289838d3e5">ISyncMgrConflictResolveInfo::GetPresenterChoice</a>
 

 

