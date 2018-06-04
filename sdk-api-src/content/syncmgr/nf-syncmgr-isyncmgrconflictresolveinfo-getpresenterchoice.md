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

# ISyncMgrConflictResolveInfo::GetPresenterChoice


## -description


Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.


## -parameters




### -param pnPresenterChoice [out]

Type: <b><a href="https://msdn.microsoft.com/5e98754b-51d7-4798-9c69-8a9a839c4cda">SYNCMGR_PRESENTER_CHOICE</a>*</b>

When this method returns, contains a pointer to the choice that was made about the conflict resolution. One of the members of the <a href="https://msdn.microsoft.com/5e98754b-51d7-4798-9c69-8a9a839c4cda">SYNCMGR_PRESENTER_CHOICE</a> enumeration.


### -param pfApplyToAll [out]

Type: <b>BOOL*</b>

When this method returns, contains a pointer to a flag. If <b>TRUE</b>, then the given choice is to be applied to all subsequent conflicts in the set, and <a href="https://msdn.microsoft.com/3c857e53-756b-44c2-b3fa-6d57c21939e7">ISyncMgrConflictResolveInfo::GetItemChoice</a> and <a href="https://msdn.microsoft.com/7604455c-35ab-4f94-8e5a-3f6aa83fc9cf">ISyncMgrConflictResolveInfo::GetItemChoiceCount</a> have information on how to apply this choice. Otherwise <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/5f4bfe69-1ff3-4d21-9c27-f5d8ecfc8371">ISyncMgrConflictResolveInfo::SetPresenterChoice</a>
 

 

