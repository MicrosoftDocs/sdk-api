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

# _DXGI_OFFER_RESOURCE_PRIORITY enumeration


## -description



          Identifies the importance of a resource’s content when you call the  <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a> method to offer the resource.
        


## -enum-fields




### -field DXGI_OFFER_RESOURCE_PRIORITY_LOW

The resource is low priority. The operating system discards a low priority resource before other offered resources with higher priority. It is a good programming practice to mark a resource as low priority if it has no useful content.


### -field DXGI_OFFER_RESOURCE_PRIORITY_NORMAL

The resource is normal priority. You mark a resource as normal priority if it has  content that is easy to regenerate.


### -field DXGI_OFFER_RESOURCE_PRIORITY_HIGH

The resource is high priority. The operating system discards other offered resources with lower priority before it discards a high priority resource.  You mark a resource as high priority if it has useful content that is difficult to regenerate.


## -remarks



Priority determines how likely the operating system is to discard an offered resource.  Resources offered with lower priority are discarded first.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a>



<a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">IDXGIDevice2::ReclaimResource</a>
 

 

