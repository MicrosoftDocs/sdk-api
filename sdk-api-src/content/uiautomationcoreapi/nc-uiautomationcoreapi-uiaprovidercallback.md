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

# UiaProviderCallback callback function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>An application-defined function that is called by UI Automation 
		to obtain a client-side provider for an element.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window served by the provider.


### -param providerType [in]

Type: <b><a href="https://msdn.microsoft.com/442dcda2-046d-4203-aa55-ddf83983cb26">ProviderType</a></b>

A value from the <a href="https://msdn.microsoft.com/442dcda2-046d-4203-aa55-ddf83983cb26">ProviderType</a> enumerated type specifying the type of provider that is being requested.


## -returns



Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a></b>

A <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing the requested provider.



