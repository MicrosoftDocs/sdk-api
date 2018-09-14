---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetPresenterChoice
title: ISyncMgrConflictResolveInfo::GetPresenterChoice
author: windows-sdk-content
description: Gets what kind of choice was made and whether to apply the choice to all subsequent conflicts in the set.
old-location: shell\ISyncMgrConflictResolveInfo_GetPresenterChoice.htm
tech.root: shell
ms.assetid: 277eee0e-3f75-4ed1-8df2-75289838d3e5
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetPresenterChoice, GetPresenterChoice method [Windows Shell], GetPresenterChoice method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetPresenterChoice method, ISyncMgrConflictResolveInfo.GetPresenterChoice, ISyncMgrConflictResolveInfo::GetPresenterChoice, _shell_ISyncMgrConflictResolveInfo_GetPresenterChoice, shell.ISyncMgrConflictResolveInfo_GetPresenterChoice, syncmgr/ISyncMgrConflictResolveInfo::GetPresenterChoice
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
 - ISyncMgrConflictResolveInfo.GetPresenterChoice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

