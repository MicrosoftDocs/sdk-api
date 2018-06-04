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

# DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration


## -description


Describes which levels of hardware composition are supported.


## -enum-fields




### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN

This flag specifies that swapchain composition can be facilitated in a performant manner using hardware for fullscreen applications.


### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED

This flag specifies that swapchain composition can be facilitated in a performant manner using hardware for windowed applications.


### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED

This flag specifies that swapchain composition facilitated using hardware can cause the cursor to appear stretched.


## -remarks



Values of this enumeration are returned from the <a href="direct3ddxgi.idxgioutput6_checkhardwarecompositionsupport">IDXGIOutput6::CheckHardwareCompositionSupport</a> method in the <i>pFlags</i> out parameter.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>



<a href="direct3ddxgi.idxgioutput6_checkhardwarecompositionsupport">IDXGIOutput6::CheckHardwareCompositionSupport method</a>
 

 

