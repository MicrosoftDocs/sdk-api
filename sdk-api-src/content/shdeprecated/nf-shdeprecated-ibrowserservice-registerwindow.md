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

# IBrowserService::RegisterWindow


## -description


Deprecated. Registers the browser in the list of browser windows.


## -parameters




### -param fForceRegister

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether to reregister the browser window if it was previously registered. If set to <b>TRUE</b> and the window was previously registered, this method will unregister and reregister the browser window.



#### TRUE

Force the window to be unregistered then reregistered.



#### FALSE

If the window is already registered, do nothing.


### -param swc

Type: <b>int</b>

One of the <a href="https://msdn.microsoft.com/79d4fcf3-5256-4e21-ab9a-94605e1d742f">ShellWindowTypeConstants</a> values to indicate the nature of the window. Note that these values are defined in Expdisp.h.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



