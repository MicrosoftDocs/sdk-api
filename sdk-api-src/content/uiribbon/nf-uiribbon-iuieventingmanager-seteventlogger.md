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

# IUIEventingManager::SetEventLogger


## -description


Sets the event logger for ribbon events.


## -parameters




### -param eventLogger [in]

The event logger.

If NULL, disables event logging.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <a href="https://msdn.microsoft.com/bb6525dd-7e05-40e0-bdcc-c66f31a99f46">IUIFramework::Initialize</a> and <a href="https://msdn.microsoft.com/d8860459-ad4d-4783-9fef-25d313bc15c7">IUIFramework::LoadUI</a> before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/54DB1BFF-0657-4027-8C8C-89CE998253F4">IUIEventLogger</a>



<a href="https://msdn.microsoft.com/11E53D75-B8C0-40A3-8E4D-ACAA10BEAC84">IUIEventingManager</a>
 

 

