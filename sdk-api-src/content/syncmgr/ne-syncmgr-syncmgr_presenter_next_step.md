---
UID: NE:syncmgr.SYNCMGR_PRESENTER_NEXT_STEP
title: SYNCMGR_PRESENTER_NEXT_STEP
author: windows-sdk-content
description: Describes the next step that is to occur in sync manager conflict resolution. Used by ISyncMgrConflictPresenter.
old-location: shell\SYNCMGR_PRESENTER_NEXT_STEP.htm
tech.root: shell
ms.assetid: e24b09e0-38a1-421b-8cf1-74f553cf93e7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SYNCMGR_PNS_CANCEL, SYNCMGR_PNS_CONTINUE, SYNCMGR_PNS_DEFAULT, SYNCMGR_PRESENTER_NEXT_STEP, SYNCMGR_PRESENTER_NEXT_STEP enumeration [Windows Shell], _shell_SYNCMGR_PRESENTER_NEXT_STEP, shell.SYNCMGR_PRESENTER_NEXT_STEP, syncmgr/SYNCMGR_PNS_CANCEL, syncmgr/SYNCMGR_PNS_CONTINUE, syncmgr/SYNCMGR_PNS_DEFAULT, syncmgr/SYNCMGR_PRESENTER_NEXT_STEP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_PRESENTER_NEXT_STEP
product: Windows
targetos: Windows
req.typenames: SYNCMGR_PRESENTER_NEXT_STEP
req.redist: 
---

# SYNCMGR_PRESENTER_NEXT_STEP enumeration


## -description


Describes the next step that is to occur in sync manager conflict resolution. Used by <a href="https://msdn.microsoft.com/ec9a2050-23ad-4478-a705-0a7324e8f84d">ISyncMgrConflictPresenter</a>.


## -enum-fields




### -field SYNCMGR_PNS_CONTINUE

The conflict has been resolved and subsequent
selected conflicts should continue to be resolved.


### -field SYNCMGR_PNS_DEFAULT

The default conflict presenter should be used.


### -field SYNCMGR_PNS_CANCEL

All conflict resolution should be canceled.


## -see-also




<a href="https://msdn.microsoft.com/7f263f83-1d7c-40c6-a57c-1334a52cd712">ISyncMgrConflictResolveInfo::GetPresenterNextStep</a>



<a href="https://msdn.microsoft.com/a56ca252-89e5-4ad0-bc9a-f8c7b70bd536">ISyncMgrConflictResolveInfo::SetPresenterNextStep</a>
 

 

