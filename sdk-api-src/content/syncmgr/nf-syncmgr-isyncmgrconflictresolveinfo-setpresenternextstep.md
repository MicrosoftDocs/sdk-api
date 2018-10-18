---
UID: NF:syncmgr.ISyncMgrConflictResolveInfo.SetPresenterNextStep
title: ISyncMgrConflictResolveInfo::SetPresenterNextStep
author: windows-sdk-content
description: Sets what the presenter wants to do as the next step in the sync manager conflict resolution.
old-location: shell\ISyncMgrConflictResolveInfo_SetPresenterNextStep.htm
tech.root: shell
ms.assetid: a56ca252-89e5-4ad0-bc9a-f8c7b70bd536
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ISyncMgrConflictResolveInfo interface [Windows Shell],SetPresenterNextStep method, ISyncMgrConflictResolveInfo.SetPresenterNextStep, ISyncMgrConflictResolveInfo::SetPresenterNextStep, SetPresenterNextStep, SetPresenterNextStep method [Windows Shell], SetPresenterNextStep method [Windows Shell],ISyncMgrConflictResolveInfo interface, _shell_ISyncMgrConflictResolveInfo_SetPresenterNextStep, shell.ISyncMgrConflictResolveInfo_SetPresenterNextStep, syncmgr/ISyncMgrConflictResolveInfo::SetPresenterNextStep
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
 - ISyncMgrConflictResolveInfo.SetPresenterNextStep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrConflictResolveInfo::SetPresenterNextStep


## -description


Sets what the presenter wants to do as the next step in the sync manager conflict resolution.


## -parameters




### -param nPresenterNextStep [in]

Type: <b><a href="https://msdn.microsoft.com/e24b09e0-38a1-421b-8cf1-74f553cf93e7">SYNCMGR_PRESENTER_NEXT_STEP</a></b>

The next step in the conflict resolution. One of the members of the <a href="https://msdn.microsoft.com/e24b09e0-38a1-421b-8cf1-74f553cf93e7">SYNCMGR_PRESENTER_NEXT_STEP</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/7f263f83-1d7c-40c6-a57c-1334a52cd712">ISyncMgrConflictResolveInfo::GetPresenterNextStep</a>
 

 

