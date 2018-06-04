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
 

 

