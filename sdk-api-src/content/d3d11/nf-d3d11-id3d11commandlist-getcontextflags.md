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

# ID3D11CommandList::GetContextFlags


## -description


Gets the initialization flags associated with the deferred context that created the command list.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The context flag is reserved for future use and is always 0.




## -remarks



The GetContextFlags method gets the flags that were supplied to the <i>ContextFlags</i> parameter of <a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">ID3D11Device::CreateDeferredContext</a>; however, the context flag is reserved for future use.




## -see-also




<a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a>
 

 

