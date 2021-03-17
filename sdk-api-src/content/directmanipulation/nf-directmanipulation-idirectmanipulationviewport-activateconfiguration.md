---
UID: NF:directmanipulation.IDirectManipulationViewport.ActivateConfiguration
title: IDirectManipulationViewport::ActivateConfiguration (directmanipulation.h)
description: Sets the configuration for input interaction.
helpviewer_keywords: ["ActivateConfiguration","ActivateConfiguration method [Direct Manipulation]","ActivateConfiguration method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","ActivateConfiguration method","IDirectManipulationViewport.ActivateConfiguration","IDirectManipulationViewport::ActivateConfiguration","directmanipulation.idirectmanipulationviewport_activateconfiguration","directmanipulation/IDirectManipulationViewport::ActivateConfiguration"]
old-location: directmanipulation\idirectmanipulationviewport_activateconfiguration.htm
tech.root: directmanipulation
ms.assetid: 16c5902d-dddd-4c40-b1f9-cb432940aa3d
ms.date: 12/05/2018
ms.keywords: ActivateConfiguration, ActivateConfiguration method [Direct Manipulation], ActivateConfiguration method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],ActivateConfiguration method, IDirectManipulationViewport.ActivateConfiguration, IDirectManipulationViewport::ActivateConfiguration, directmanipulation.idirectmanipulationviewport_activateconfiguration, directmanipulation/IDirectManipulationViewport::ActivateConfiguration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationViewport::ActivateConfiguration
 - directmanipulation/IDirectManipulationViewport::ActivateConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.ActivateConfiguration
---

# IDirectManipulationViewport::ActivateConfiguration


## -description

Sets the configuration for input interaction.

## -parameters

### -param configuration [in]

One or more values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration">DIRECTMANIPULATION_CONFIGURATION</a> that specify the interaction configuration for the viewport.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An interaction configuration specifies how the manipulation engine responds to input and which manipulations are supported. Any number of possible configurations can be added to the viewport using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a> before processing input. 

Configurations can be switched by the application at runtime using <b>ActivateConfiguration</b>.  

When a configuration is no longer required (and is not currently active), it can be removed using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>. 

If a configuration has not been added using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>, it can be automatically added and then activated by calling <b>ActivateConfiguration</b>. 

<div class="alert"><b>Note</b>  If input processing is occurring, this call will fail.</div>
<div> </div>
This method fails if a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-guids">drag and drop</a> behavior has been specified. 

A <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-guids">drag and drop</a> behavior object cannot be attached after successfully calling this method.


#### Examples

The following example shows how to configure a viewport for horizontal panning.


```
HRESULT hr = pViewport>ActivateConfiguration(
    DIRECTMANIPULATION_CONFIGURATION_INTERACTION | 
    DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>