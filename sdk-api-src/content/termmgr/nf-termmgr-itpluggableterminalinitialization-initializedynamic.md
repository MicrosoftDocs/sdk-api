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

# ITPluggableTerminalInitialization::InitializeDynamic


## -description


The 
<b>InitializeDynamic</b> method performs primary terminal object creation for the pluggable terminal.


## -parameters




### -param iidTerminalClass [in]

The IID_ for the class of the terminal being initialized.


### -param dwMediaType [in]

ORed list of the media types supported by the terminal.


### -param Direction [in]

The 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor for the terminal.


### -param htAddress [in]

MSP handle for the address to associate with the terminal being created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc1e6fb7-1b2a-40bd-83a8-d3b8be93ddc0">ITPluggableTerminalInitialization</a>
 

 

