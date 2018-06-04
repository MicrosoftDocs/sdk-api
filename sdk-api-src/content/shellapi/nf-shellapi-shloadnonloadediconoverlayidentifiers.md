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

# SHLoadNonloadedIconOverlayIdentifiers function


## -description


Signals the Shell that during the next operation requiring overlay information, it should load icon overlay identifiers that either failed creation or were not present for creation at startup. Identifiers that have already been loaded are not affected.


## -parameters






## -returns



Type: <b>HRESULT</b>

Always returns S_OK.




## -remarks



A call to <b>SHLoadNonloadedIconOverlayIdentifiers</b> does not result in the immediate loading of a Shell extension, nor does it cause an icon overlay handler to be loaded. A call to <b>SHLoadNonloadedIconOverlayIdentifiers</b> results in a situation such that the next code to ask for icon overlay information triggers a comparison of icon overlays in the registry to those that are already loaded. If an icon overlay is newly registered and the system has not already reached its upper limit of fifteen icon overlays, the new overlay is loaded. <b>SHLoadNonloadedIconOverlayIdentifiers</b> alone does not load a new icon overlay; you also need to trigger an action that uses the overlay, such as a refresh of a Windows Explorer view.

For more information, see <a href="https://msdn.microsoft.com/ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92">How to Implement Icon Overlay Handlers</a>.



