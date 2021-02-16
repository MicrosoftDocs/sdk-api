---
UID: NF:directmanipulation.IDirectManipulationViewport.RemoveConfiguration
title: IDirectManipulationViewport::RemoveConfiguration (directmanipulation.h)
description: Removes an interaction configuration for the viewport.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","RemoveConfiguration method","IDirectManipulationViewport.RemoveConfiguration","IDirectManipulationViewport::RemoveConfiguration","RemoveConfiguration","RemoveConfiguration method [Direct Manipulation]","RemoveConfiguration method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_removeconfiguration","directmanipulation/IDirectManipulationViewport::RemoveConfiguration"]
old-location: directmanipulation\idirectmanipulationviewport_removeconfiguration.htm
tech.root: directmanipulation
ms.assetid: 2aac9468-a060-4f06-9e8e-139355be75f7
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],RemoveConfiguration method, IDirectManipulationViewport.RemoveConfiguration, IDirectManipulationViewport::RemoveConfiguration, RemoveConfiguration, RemoveConfiguration method [Direct Manipulation], RemoveConfiguration method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_removeconfiguration, directmanipulation/IDirectManipulationViewport::RemoveConfiguration
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
 - IDirectManipulationViewport::RemoveConfiguration
 - directmanipulation/IDirectManipulationViewport::RemoveConfiguration
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
 - IDirectManipulationViewport.RemoveConfiguration
---

# IDirectManipulationViewport::RemoveConfiguration


## -description

Removes an interaction configuration for the viewport.

## -parameters

### -param configuration [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration">DIRECTMANIPULATION_CONFIGURATION</a> that specifies the interaction configuration for the viewport.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method removes a possible configuration that was added by using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>. This method can be called only if the configuration is not active.

An interaction configuration specifies how the manipulation engine responds to input and which gestures are supported. Any number of configurations can be added to the viewport using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>. Configurations can be switched by the application at runtime using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>. When a configuration is no longer required (and is not currently active), it can be removed using <b>RemoveConfiguration</b>.


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pRegion->RemoveConfiguration(
    DIRECTMANIPULATION_CONFIGURATION_INTERACTION | 
    DIRECTMANIPULATION_CONFIGURATION_TRANSLATION_X);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>