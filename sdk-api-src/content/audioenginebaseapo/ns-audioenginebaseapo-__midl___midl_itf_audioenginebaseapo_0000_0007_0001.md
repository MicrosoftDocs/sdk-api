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

# __MIDL___MIDL_itf_audioenginebaseapo_0000_0007_0001 structure


## -description


The AudioFXExtensionParams structure is passed to the system effects ControlPanel  
Extension PropertyPage via <a href="http://msdn.microsoft.com/en-us/library/windows/hardware/bb416595.aspx">IShellPropSheetExt::AddPages</a>.


## -struct-fields




### -field AddPageParam

Parameters for the Property Page extension.


### -field pwstrEndpointID

The ID for the audio endpoint.


### -field pFxProperties

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>



<a href="http://msdn.microsoft.com/en-us/library/windows/hardware/bb416595.aspx">IShellPropSheetExt::AddPages</a>
 

 

