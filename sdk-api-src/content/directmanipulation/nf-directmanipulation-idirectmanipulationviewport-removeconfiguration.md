---
UID: NF:directmanipulation.IDirectManipulationViewport.RemoveConfiguration
title: IDirectManipulationViewport::RemoveConfiguration
author: windows-sdk-content
description: Removes an interaction configuration for the viewport.
old-location: directmanipulation\idirectmanipulationviewport_removeconfiguration.htm
tech.root: directmanipulation
ms.assetid: 2aac9468-a060-4f06-9e8e-139355be75f7
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],RemoveConfiguration method, IDirectManipulationViewport.RemoveConfiguration, IDirectManipulationViewport::RemoveConfiguration, RemoveConfiguration, RemoveConfiguration method [Direct Manipulation], RemoveConfiguration method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_removeconfiguration, directmanipulation/IDirectManipulationViewport::RemoveConfiguration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.RemoveConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::RemoveConfiguration


## -description


Removes an interaction configuration for the viewport.


## -parameters




### -param configuration [in]

One of the values from <a href="https://msdn.microsoft.com/a7c146e8-a1df-4445-8230-1dd491d0e9a3">DIRECTMANIPULATION_CONFIGURATION</a> that specifies the interaction configuration for the viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method removes a possible configuration that was added by using <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>. This method can be called only if the configuration is not active.

An interaction configuration specifies how the manipulation engine responds to input and which gestures are supported. Any number of configurations can be added to the viewport using <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>. Configurations can be switched by the application at runtime using <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>. When a configuration is no longer required (and is not currently active), it can be removed using <b>RemoveConfiguration</b>.


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pRegion->RemoveConfiguration(
    DIRECTMANIPULATION_CONFIGURATION_INTERACTION | 
    DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X);

```





## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

