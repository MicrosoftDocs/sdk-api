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

# __MIDL___MIDL_itf_mmdeviceapi_0000_0008_0001 structure


## -description


This structure is passed to the Control Panel Endpoint Extension property page through <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a> and is used to create endpoint PropertyPages.


## -struct-fields




### -field AddPageParam

The add page param.


### -field pEndpoint

Pointer to the end point.


### -field pPnpInterface

Pointer to the Pnp interface.


### -field pPnpDevnode

Pointer to the Pnp devnode.


## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a>
 

 

