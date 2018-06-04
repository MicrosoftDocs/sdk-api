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

# ILaunchTargetViewSizePreference::GetTargetViewSizePreference


## -description


Retrieves the preferred view size of the application being launched.


## -parameters




### -param targetSizeOnLaunch [out]

Type: <b><a href="https://msdn.microsoft.com/20B27858-D5BC-4800-AE3F-C01A017ABBF7">APPLICATION_VIEW_SIZE_PREFERENCE</a>*</b>

Contains the address of a pointer to an <a href="https://msdn.microsoft.com/20B27858-D5BC-4800-AE3F-C01A017ABBF7">APPLICATION_VIEW_SIZE_PREFERENCE</a>  for the target application.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3535E9EF-265E-4278-8E0D-60AA8A34C316">ILaunchTargetViewSizePreference</a>
 

 

