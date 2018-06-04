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

# ISyncMgrConflictResolveInfo::GetPresenterNextStep


## -description


Gets what the presenter wants to do as the next step in the sync manager conflict resolution.


## -parameters




### -param pnPresenterNextStep [out]

Type: <b><a href="https://msdn.microsoft.com/e24b09e0-38a1-421b-8cf1-74f553cf93e7">SYNCMGR_PRESENTER_NEXT_STEP</a>*</b>

When this method returns, contains a pointer to the next step in conflict resolution. One of the members of the <a href="https://msdn.microsoft.com/e24b09e0-38a1-421b-8cf1-74f553cf93e7">SYNCMGR_PRESENTER_NEXT_STEP</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c47d533f-7307-4db3-a025-961f3419203e">ISyncMgrConflictResolveInfo</a>



<a href="https://msdn.microsoft.com/a56ca252-89e5-4ad0-bc9a-f8c7b70bd536">ISyncMgrConflictResolveInfo::SetPresenterNextStep</a>
 

 

