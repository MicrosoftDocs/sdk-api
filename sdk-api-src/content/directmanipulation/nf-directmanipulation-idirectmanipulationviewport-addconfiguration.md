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

# IDirectManipulationViewport::AddConfiguration


## -description


Adds an interaction configuration for the viewport.


## -parameters




### -param configuration [in]

One of the values from <a href="https://msdn.microsoft.com/a7c146e8-a1df-4445-8230-1dd491d0e9a3">DIRECTMANIPULATION_CONFIGURATION</a> that specifies the interaction configuration for the viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



An interaction configuration specifies how the manipulation engine responds to input and which manipulations are supported. Any number of possible configurations can be added to the viewport using <b>AddConfiguration</b> before processing input. 

Configurations can be switched by the application at runtime using <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>.  

When a configuration is no longer required (and is not currently active), it can be removed using <a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>. 

If a configuration has not been added using <b>AddConfiguration</b>, it can be automatically added and then activated by calling <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>. 

<div class="alert"><b>Note</b>  If input processing is occurring, this call will fail.</div>
<div> </div>
This method fails if a <a href="https://msdn.microsoft.com/6747D082-4B7B-4C7E-A230-2E8C8412FABD">drag and drop</a> behavior has been specified. 

A <a href="https://msdn.microsoft.com/6747D082-4B7B-4C7E-A230-2E8C8412FABD">drag and drop</a> behavior object cannot be attached after successfully calling this method.

You cannot add another <a href="https://msdn.microsoft.com/6747D082-4B7B-4C7E-A230-2E8C8412FABD">drag and drop</a> behavior after an existing one has already been added.

This method is designed to allow an application to switch pre-added configurations, as a configuration cannot be changed while a manipulation is occurring. Under most circumstances it is better to update the configuration using <a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

