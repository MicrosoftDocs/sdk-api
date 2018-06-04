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

# _DXGI_RECLAIM_RESOURCE_RESULTS enumeration


## -description


Specifies result flags for the <a href="https://msdn.microsoft.com/83D09C41-CB96-4ADA-AE38-7D9542CCCFE0">ReclaimResources1</a> method.


## -enum-fields




### -field DXGI_RECLAIM_RESOURCE_RESULT_OK

The surface was successfully reclaimed and has valid content. This result is identical to the <i>false</i> value returned by the older <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a> API.


### -field DXGI_RECLAIM_RESOURCE_RESULT_DISCARDED

The surface was reclaimed, but the old content was lost and must be regenerated. This result is identical to the <i>true</i> value returned by the older <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a> API.


### -field DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED

 Both the surface and its contents are lost and invalid. The surface must be 
recreated and the content regenerated in order to be used. All future use of that resource is invalid. Attempts to bind it to the pipeline or map a resource which returns this value will never succeed, and the resource cannot be reclaimed again.


## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

