---
UID: NF:directmanipulation.IDirectManipulationViewport.ActivateConfiguration
title: IDirectManipulationViewport::ActivateConfiguration
author: windows-sdk-content
description: Sets the configuration for input interaction.
old-location: directmanipulation\idirectmanipulationviewport_activateconfiguration.htm
tech.root: directmanipulation
ms.assetid: 16c5902d-dddd-4c40-b1f9-cb432940aa3d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ActivateConfiguration, ActivateConfiguration method [Direct Manipulation], ActivateConfiguration method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],ActivateConfiguration method, IDirectManipulationViewport.ActivateConfiguration, IDirectManipulationViewport::ActivateConfiguration, directmanipulation.idirectmanipulationviewport_activateconfiguration, directmanipulation/IDirectManipulationViewport::ActivateConfiguration
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
 - IDirectManipulationViewport.ActivateConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::ActivateConfiguration


## -description


Sets the configuration for input interaction.


## -parameters




### -param configuration [in]

One or more values from <a href="https://msdn.microsoft.com/a7c146e8-a1df-4445-8230-1dd491d0e9a3">DIRECTMANIPULATION_CONFIGURATION</a> that specify the interaction configuration for the viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



An interaction configuration specifies how the manipulation engine responds to input and which manipulations are supported. Any number of possible configurations can be added to the viewport using <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a> before processing input. 

Configurations can be switched by the application at runtime using <b>ActivateConfiguration</b>.  

When a configuration is no longer required (and is not currently active), it can be removed using <a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>. 

If a configuration has not been added using <a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>, it can be automatically added and then activated by calling <b>ActivateConfiguration</b>. 

<div class="alert"><b>Note</b>  If input processing is occurring, this call will fail.</div>
<div> </div>
This method fails if a <a href="https://msdn.microsoft.com/6747D082-4B7B-4C7E-A230-2E8C8412FABD">drag and drop</a> behavior has been specified. 

A <a href="https://msdn.microsoft.com/6747D082-4B7B-4C7E-A230-2E8C8412FABD">drag and drop</a> behavior object cannot be attached after successfully calling this method.


#### Examples

The following example shows how to configure a viewport for horizontal panning.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT hr = pViewport&gt;ActivateConfiguration(
    DIRECTMANIPULATION_CONFIGURATION_INTERACTION | 
    DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

