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

# IApplicationDesignModeSettings2::GetApplicationViewOrientation


## -description


Gets the orientation of the application design mode window.


## -parameters




### -param applicationSizePixels




### -param viewOrientation [out]

Type: <b><a href="https://msdn.microsoft.com/6E14D892-09E3-46F4-84AD-991996431FB2">APPLICATION_VIEW_ORIENTATION</a>*</b>

When this method returns successfully, receives a pointer to an  <a href="https://msdn.microsoft.com/6E14D892-09E3-46F4-84AD-991996431FB2">APPLICATION_VIEW_ORIENTATION</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1F630AFF-3C73-461C-AE41-D597F6FF42D8">IApplicationDesignModeSettings2</a>
 

 

