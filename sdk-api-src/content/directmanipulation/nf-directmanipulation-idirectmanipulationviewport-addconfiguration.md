---
UID: NF:directmanipulation.IDirectManipulationViewport.AddConfiguration
title: IDirectManipulationViewport::AddConfiguration (directmanipulation.h)
description: Adds an interaction configuration for the viewport.
helpviewer_keywords: ["AddConfiguration","AddConfiguration method [Direct Manipulation]","AddConfiguration method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","AddConfiguration method","IDirectManipulationViewport.AddConfiguration","IDirectManipulationViewport::AddConfiguration","directmanipulation.idirectmanipulationviewport_addconfiguration","directmanipulation/IDirectManipulationViewport::AddConfiguration"]
old-location: directmanipulation\idirectmanipulationviewport_addconfiguration.htm
tech.root: directmanipulation
ms.assetid: 908f67ef-3606-4636-88aa-4e95d80a9c7a
ms.date: 12/05/2018
ms.keywords: AddConfiguration, AddConfiguration method [Direct Manipulation], AddConfiguration method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],AddConfiguration method, IDirectManipulationViewport.AddConfiguration, IDirectManipulationViewport::AddConfiguration, directmanipulation.idirectmanipulationviewport_addconfiguration, directmanipulation/IDirectManipulationViewport::AddConfiguration
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
 - IDirectManipulationViewport::AddConfiguration
 - directmanipulation/IDirectManipulationViewport::AddConfiguration
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
 - IDirectManipulationViewport.AddConfiguration
---

# IDirectManipulationViewport::AddConfiguration


## -description

Adds an interaction configuration for the viewport.

## -parameters

### -param configuration [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration">DIRECTMANIPULATION_CONFIGURATION</a> that specifies the interaction configuration for the viewport.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An interaction configuration specifies how the manipulation engine responds to input and which manipulations are supported. Any number of possible configurations can be added to the viewport using <b>AddConfiguration</b> before processing input. 

Configurations can be switched by the application at runtime using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>.  

When a configuration is no longer required (and is not currently active), it can be removed using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>. 

If a configuration has not been added using <b>AddConfiguration</b>, it can be automatically added and then activated by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>. 

<div class="alert"><b>Note</b>  If input processing is occurring, this call will fail.</div>
<div> </div>
This method fails if a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-guids">drag and drop</a> behavior has been specified. 

A <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-guids">drag and drop</a> behavior object cannot be attached after successfully calling this method.

You cannot add another <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-guids">drag and drop</a> behavior after an existing one has already been added.

This method is designed to allow an application to switch pre-added configurations, as a configuration cannot be changed while a manipulation is occurring. Under most circumstances it is better to update the configuration using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>