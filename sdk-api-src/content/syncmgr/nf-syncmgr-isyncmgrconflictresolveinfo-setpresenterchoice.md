---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

