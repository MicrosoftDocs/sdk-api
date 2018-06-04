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

# ILaunchSourceAppUserModelId::GetAppUserModelId


## -description


Retrieves an <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a> from the source application.


## -parameters




### -param launchingApp [out]

Type: <b>LPWSTR*</b>

Contains a  pointer to a string that contains the <a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">AppUserModelId</a>



<a href="https://msdn.microsoft.com/B53325C9-DC89-4411-82D9-247C28AFB177">ILaunchSourceAppUserModelId</a>
 

 

