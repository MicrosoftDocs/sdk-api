---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.GetItemChoiceCount
title: ISyncMgrConflictResolveInfo::GetItemChoiceCount
author: windows-sdk-content
description: Gets the number of items that the user wants to keep.
old-location: shell\ISyncMgrConflictResolveInfo_GetItemChoiceCount.htm
tech.root: shell
ms.assetid: 7604455c-35ab-4f94-8e5a-3f6aa83fc9cf
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: GetItemChoiceCount, GetItemChoiceCount method [Windows Shell], GetItemChoiceCount method [Windows Shell],ISyncMgrConflictResolveInfo interface, ISyncMgrConflictResolveInfo interface [Windows Shell],GetItemChoiceCount method, ISyncMgrConflictResolveInfo.GetItemChoiceCount, ISyncMgrConflictResolveInfo::GetItemChoiceCount, _shell_ISyncMgrConflictResolveInfo_GetItemChoiceCount, shell.ISyncMgrConflictResolveInfo_GetItemChoiceCount, syncmgr/ISyncMgrConflictResolveInfo::GetItemChoiceCount
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
 - ISyncMgrConflictResolveInfo.GetItemChoiceCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflictResolveInfo::GetItemChoiceCount


## -description


Gets the number of items that the user wants to keep.


## -parameters




### -param pcChoices [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of items that the user wants to keep.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/3c857e53-756b-44c2-b3fa-6d57c21939e7">ISyncMgrConflictResolveInfo::GetItemChoice</a>



<a href="https://msdn.microsoft.com/e4485f49-9bcb-47a8-8559-da2217ee1eab">ISyncMgrConflictResolveInfo::SetItemChoices</a>
 

 

